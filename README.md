# Receitas do Grupo

Projeto simples para abrir o site com Live Server no VS Code e usar Python Flask + MySQL no banco.

## 1. Preparar o banco de dados
1. Abra o MySQL Workbench.
2. Abra `banco/script.sql`.
3. Execute o script inteiro. Ele cria o banco `receitas_grupo`, as tabelas e seis receitas de exemplo.

## 2. Configurar o Flask
1. Instale Python 3.
2. Abra `flask/app.py`.
3. Troque `SUA_SENHA_AQUI` pela senha do seu MySQL. Se necessário, altere o usuário `root`.
4. Abra o terminal do VS Code na pasta `flask`.
5. Execute:

```bash
python -m pip install -r requirements.txt
python app.py
```

Se aparecer que o servidor está rodando em `http://127.0.0.1:5000`, o Flask está ligado. Não feche esse terminal.

## 3. Abrir o site com Live Server
1. No VS Code, abra a pasta principal `receitas-grupo`.
2. Clique com o botão direito em `index.html`.
3. Escolha **Open with Live Server**.
4. O site abre no navegador e busca os dados do Flask.

## Como iniciar no dia a dia
- Primeiro: iniciar o MySQL (por exemplo, abrir o MySQL Workbench/serviço MySQL).
- Segundo: executar `python app.py` dentro da pasta `flask`.
- Terceiro: abrir `index.html` com Live Server.

## O que funciona
- Listar receitas cadastradas no MySQL.
- Cadastrar receita e seus ingredientes.
- Alterar o status para rascunho, testada ou favorita.
- Editar o nome da receita.
- Excluir receita.
- Filtrar por status e atualizar os contadores.

## Observação
O Live Server serve apenas os arquivos HTML, CSS e JavaScript. Quem conversa com o MySQL é o Flask. Por isso os dois servidores precisam ficar ligados. O projeto usa o usuário de exemplo `1` na tabela `usuarios`, criado pelo script SQL; não há sistema de login.
