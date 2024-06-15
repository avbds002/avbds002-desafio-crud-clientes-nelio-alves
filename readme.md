<h1>Desafio proposta pelo professor Nelio Alves em seu bootcamp de Java Spring Boot</h1>

<p>A proposta da atividade consistem em criar um CRUD completo de web services REST para acessar um recurso de clientes, contendo as cinco operações básicas de um CRUD completo.</p>
<ol>
    <li>Busca paginada de recursos</li>
    <li>Busca de recurso por ID</li>
    <li>Inserir um novo recurso</li>
    <li>Atualizar recurso</li>
    <li>Deletar recurso</li>
</ol>
<hr>
<h2>Especificações da atividade</h2>
<p>O projeto deverá estar com um ambiente de testes configurado acessando o banco de dados H2, deverá usar Maven como gerenciador de dependência, e Java como linguagem.</p>
<p><b>É necessário fazer um seed no banco de dados de pelo menos 10 clientes com dados SIGNIFICATIVOS (não utilizar dados sem significado como por exemplo: "Nome 1", "Nome 2", etc..</b></p>
<p><b>Seu projeto deverá tratar as seguintes exceções:</b></p>
<ul>
    <li>Id não encontrado (para GET por id, PUT e DELETE), retornando código 404</li>
    <li>Erro de validação, retornando código 422 e mensagens customizadas para cada campo inválido.</li>
    <li>As regras de validação são: <strong>Nome não pode ser vazio, Data de nascimento não pode ser data futura</strong></li>
</ul>
<hr>
<h2>Modelo da classe Client</h2>
<p>colocar imagem aqui</p>
<hr>
<h2>Testes manuais no POSTMAN</h2>
<p style="background-color: red; border-radius:5px; padding: 5px; color: black; font-weight: 600">Busca de cliente por id</p>
<p style="background-color: yellow; border-radius:5px; padding: 5px; color: black; font-weight: 600">GET /clientes/1</p>
<p style="background-color: red; border-radius:5px; padding: 5px; color: black; font-weight: 600">Busca paginada de clientes</p>
<p style="background-color: yellow; border-radius:5px; padding: 5px; color: black; font-weight: 600">GET /clients?page=0&size=6&sort=name</p>
<p style="background-color: red; border-radius:5px; padding: 5px; color: black; font-weight: 600">Inserção de novo cliente</p>
<p style="background-color: yellow; border-radius:5px; padding: 5px; color: black; font-weight: 600">POST /clients
<br>
{
<br>
"name": "Maria Silvaaa",
<br>
"cpf": "12345678901",
<br>
"income": 6500.0,
<br>
"birthDate": "1994-07-20",
<br>
"children": 2
<br>
}
</p>
<p style="background-color: red; border-radius:5px; padding: 5px; color: black; font-weight: 600">Deleção de cliente</p>
<p style="background-color: yellow; border-radius:5px; padding: 5px; color: black; font-weight: 600">DELETE /clients/1</p>
<hr>
<h2>Checklist da aplicação: </h2>
<ol>
    <li>Busca por id retorna cliente existente</li>
    <li>Busca por id retorna 404 para cliente inexistente</li>
    <li>Busca paginada retorna listagem paginada corretamente</li>
    <li>Inserção de cliente insere cliente com dados válidos</li>
    <li>Inserção de cliente retorna 422 e mensagens customizadas com dados inválidos</li>
    <li>Atualização de cliente atualiza cliente com dados válidos</li>
    <li>Atualização de cliente retorna 404 para cliente inexistente</li>
    <li>Atualização de cliente retorna 422 e mensagens customizadas com dados inválidos</li>
    <li>Deleção de cliente deleta cliente existente</li>
    <li>Deleção de cliente retorna 404 para cliente inexistente</li>
</ol>