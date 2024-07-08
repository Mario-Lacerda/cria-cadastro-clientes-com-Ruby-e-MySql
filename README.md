# Desafio Dio - Criando um Cadastro de Clientes com Ruby e MySql



Cria um **sistema de cadastro de clientes** em **Ruby on Rails** utilizando **MySQL**. Assim como no projeto anterior, vou apresentar uma estrutura básica e alguns exemplos de implementação.



## Estrutura do Projeto:



1. **Modelo Cliente**: Representa os dados dos clientes (nome, email, telefone).

2. **Rotas e Controladores**: Gerenciam as funcionalidades de cadastro, edição, exclusão e visualização de clientes.

3. **Views**: Exibem os formulários e a lista de clientes cadastrados.

   

## Passos para Criar o Projeto:



1. **Instalação do Ruby on Rails e MySQL**:

   - Certifique-se de ter o Ruby on Rails e o MySQL instalados em sua máquina.

   - Caso ainda não tenha, siga as instruções de instalação para o seu sistema operacional.

     

2. **Criando um Novo Projeto Rails**:

   - Abra o terminal e execute o seguinte comando para criar um novo projeto Rails chamado “CadastroClientes”:

     

     ### rails new CadastroClientes

     

3. **Configurando o Banco de Dados MySQL**:

   

   - Edite o arquivo `config/database.yml` para configurar a conexão com o MySQL.

   - Substitua as informações de usuário, senha, host e nome do banco de dados de acordo com suas configurações.

     

4. **Modelagem de Dados**:

   

   - Crie um modelo chamado “Cliente” para representar os dados dos clientes:

     ```
     rails generate model Cliente nome:string email:string telefone:string
     ```

     

   - Execute a migração para criar a tabela no banco de dados:

     ```
     rails db:migrate
     ```

     

5. ### **Implementando as Funcionalidades**:

   - Crie rotas e controladores para gerenciar as funcionalidades de cadastro, edição, exclusão e visualização de clientes.
   - Implemente as views para exibir os formulários e a lista de clientes.

   

6. ### **Testando a Aplicação**:

   - Inicie o servidor Rails e teste a aplicação no navegador.
   - Verifique se as funcionalidades estão funcionando corretamente.

   

7. ## **Conclusão**:

   - Ao seguir esses passos, você terá criado um aplicativo web de cadastro de clientes utilizando Ruby on Rails e MySQL.
   - Essa aplicação pode ser expandida com outras funcionalidades, como autenticação de usuários, busca, filtros e relatórios.





Aqui está uma versão mais abrangente do **Gerenciador de Estoque** e do **Cadastro de Clientes** em Ruby:



## Gerenciador de Estoque (Estoque.rb):

Ruby



```ruby
class Produto
  attr_accessor :nome, :quantidade

  def initialize(nome, quantidade)
    @nome = nome
    @quantidade = quantidade
  end

  def adicionar(quantidade)
    @quantidade += quantidade
  end

  def vender(quantidade)
    if @quantidade >= quantidade
      @quantidade -= quantidade
      true
    else
      false
    end
  end
end

# Exemplo de uso
produto1 = Produto.new('Teclado', 50)
produto1.adicionar(10)
produto1.vender(5)
```



Código gerado por IA. Examine e use com cuidado. [Mais informações em perguntas frequentes](https://www.bing.com/new#faq).



## Cadastro de Clientes (Clientes.rb):

Ruby



```ruby
class Cliente
  attr_accessor :nome, :email, :telefone

  def initialize(nome, email, telefone)
    @nome = nome
    @email = email
    @telefone = telefone
  end

  def exibir_dados
    puts "Nome: #{@nome}"
    puts "Email: #{@email}"
    puts "Telefone: #{@telefone}"
  end
end

# Exemplo de uso
cliente1 = Cliente.new('João', 'joao@email.com', '(11) 9999-8888')
cliente1.exibir_dados
```



Código gerado por IA. Examine e use com cuidado. [Mais informações em perguntas frequentes](https://www.bing.com/new#faq).



## Programa Principal (Main.rb):

Ruby



```ruby
require_relative 'Estoque'
require_relative 'Clientes'

# Exemplo de uso dos módulos
estoque = Estoque.new
estoque.adicionar_produto('Mouse', 30)
estoque.registrar_venda('Mouse', 5)

cliente = Cliente.new('Maria', 'maria@email.com', '(21) 7777-6666')
cliente.exibir_dados
```
