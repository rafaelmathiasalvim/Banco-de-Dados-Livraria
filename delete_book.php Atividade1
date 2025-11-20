<?php
include "database.php";

$id = $_POST['id'];

$stmt = $conn->prepare("DELETE FROM livros WHERE id = ?");
$stmt->bind_param("i", $id);
$stmt->execute();

header("Location: index.php");
?>
