var express    = require('express');
var Webtask    = require('webtask-tools');
var bodyParser = require('body-parser');
var assert = require('assert');
var app = express();

app.use(bodyParser.json());

app.get('/', function (req, res) {
  console.log('hfdsa');
  assert(1, 1);
  res.status(200).send({success: "true"});
});

module.exports = Webtask.fromExpress(app);
