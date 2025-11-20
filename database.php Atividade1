<?php
$host = "localhost";
$user = "root";
$pass = "";
$dbname = "livraria";

$conn = new mysqli($host, $user, $pass);


$conn->query("CREATE DATABASE IF NOT EXISTS $dbname");

$conn = new mysqli($host, $user, $pass, $dbname);

// cria tabela se não existir
$conn->query("CREATE TABLE IF NOT EXISTS livros (
    id INT AUTO_INCREMENT PRIMARY KEY,
    titulo VARCHAR(255),
    autor VARCHAR(255),
    ano INT
)");
?>
