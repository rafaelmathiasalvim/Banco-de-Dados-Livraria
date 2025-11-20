<?php
include "database.php";

$titulo = $_POST['titulo'];
$autor  = $_POST['autor'];
$ano    = $_POST['ano'];

$stmt = $conn->prepare("INSERT INTO livros (titulo, autor, ano) VALUES (?, ?, ?)");
$stmt->bind_param("ssi", $titulo, $autor, $ano);
$stmt->execute();

header("Location: index.php");
