# NodeJsMultiVarSQLIns


var mysql = require('mysql');

var con = mysql.createConnection({
  host: "localhost",
  user: "root",
  password: "password",
  database: "project"
});


var fname = "demian";
var email = "demian@gmail.com"
var pass = "ak1234"
var lname = "hansda"


con.connect(function(err) {
  if (err) throw err;
  console.log("Connected!");



var sql = "INSERT INTO user_info (first_name, email, password, last_name) VALUES ?";
var values = [
    ['prabhash', 'prabhash@gmail.com', '12345', 'jha'],
    ['kavita', 'ksharma@gmail.com', 'kv123', 'sharma']
];
con.query(sql, [values], function(err) {
    if (err) throw err;
    con.end();
});
});
