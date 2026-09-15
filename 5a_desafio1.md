<?php

$mensagem = "";

if ($_SERVER["REQUEST_METHOD"] == "POST") {

    $nome = $_POST["nome"];
    $ano_nascimento = $_POST["ano_nascimento"];

    $ano_atual = date("Y");
    $idade = $ano_atual - $ano_nascimento;

    if ($idade >= 18) {

        $mensagem = "Acesso permitido, " . $nome . "!";

        $dados = "Nome: " . $nome . " | Ano de nascimento: " . $ano_nascimento . " | Idade: " . $idade . PHP_EOL;

        file_put_contents("log_acessos.txt", $dados, FILE_APPEND);

    } else {

        $mensagem = "Acesso negado, " . $nome . "!";
    }
}

?>

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Verificador de Maioridade</title>
</head>
<body>

    <h1>Verificador de Maioridade</h1>

    <form method="POST">

        <label for="nome">Nome:</label>
        <input type="text" id="nome" name="nome" required>

        <br><br>

        <label for="ano_nascimento">Ano de Nascimento:</label>
        <input type="number" id="ano_nascimento" name="ano_nascimento" required>

        <br><br>

        <button type="submit">Verificar</button>

    </form>

    <?php if ($mensagem != ""): ?>
        <h2><?php echo htmlspecialchars($mensagem); ?></h2>
    <?php endif; ?>

</body>
</html>