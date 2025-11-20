<?php include "database.php"; ?>
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Livraria Simples</title>
    <script>
        function confirmarExclusao() {
            return confirm("Tem certeza que deseja excluir?");
        }
    </script>
</head>
<body>

<h2>Adicionar Livro</h2>
<form action="add_book.php" method="POST">
    Título: <input type="text" name="titulo"><br><br>
    Autor: <input type="text" name="autor"><br><br>
    Ano: <input type="number" name="ano"><br><br>
    <button type="submit">Salvar</button>
</form>

<hr>

<h2>Lista de Livros</h2>

<?php
$result = $conn->query("SELECT * FROM livros");

while($livro = $result->fetch_assoc()) {
    echo "ID: ".$livro['id']." | ".
         "Título: ".$livro['titulo']." | ".
         "Autor: ".$livro['autor']." | ".
         "Ano: ".$livro['ano'];

    echo "
    <form action='delete_book.php' method='POST' style='display:inline;' onsubmit='return confirmarExclusao()'>
        <input type='hidden' name='id' value='".$livro['id']."'>
        <button type='submit'>Excluir</button>
    </form><br><br>
    ";
}
?>

</body>
</html>
