var port = process.env.PORT || 8080;

var server = require('http-server').createServer({
  root: './',
  ext: 'html'
});

server.listen(port, function () {
  console.log('Starting up http-server, serving '
    + server.root
    + ' on port: '
    + port);
});

process.on('SIGINT', function() {
  console.log('http-server stopped.');
  return process.exit();
});