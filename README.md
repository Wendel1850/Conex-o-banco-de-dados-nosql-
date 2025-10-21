# Conex-o-banco-de-dados-nosql-
// Conectar ao banco de dados
const MongoClient = require('mongodb').MongoClient;
const url = 'mongodb:                   
const dbName = '//localhost:27017';
const dbName = 'meubanco';

MongoClient.connect(url, function(err, client) {
  if (err) {
    console.log(err);
  } else {
    console.log('Conectado ao banco de dados!');
    const db = client.db(dbName);

                                   
    const collection = db.collection('// Criar uma coleção (tabela)
    const collection = db.collection('clientes');

                                   
    collection.insertOne({
      nome: '// Inserir um documento (linha)
    collection.insertOne({
      nome: 'João Silva',
      email: 'joao.silva@example.com',
      telefone: '1234567890'
    }, function(err, result) {
      if (err) {
        console.log(err);
      } else {
        console.log('Documento inserido com sucesso!');
      }
    });

    // Buscar todos os documentos
    collection.find().toArray(function(err, docs) {
      if (err) {
        console.log(err);
      } else {
        console.log(docs);
      }
    });
  }
});
