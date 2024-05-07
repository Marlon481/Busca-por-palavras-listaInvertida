#Projeto com aplicação de listas invertidas

## Descrição do que foi realizado
  Foi implementada apenas uma classe nova, utilizada para remover stopWords e retirar os acentos e caracteres especiais, mas apenas as stopWords foram excluidas.
  Alguns métodos foram alterados para atender as especificações do projeto, como por exemplo no menu foram adicionadas opções para acesso dos novos métodos criados.
Os métodos criados para atender as especificações do projeto foram:
#### Classe MenuLivros:
 Nessa classe foram criados três métodos:
 * Método 'buscarLivroTitulo' para buscar e mostrar livros por pesquisas de palavra chave(linha236);
 * Método 'alterarLivroTitulo' para buscar e mostrar alterção de um certo livro através de busca pelo título;
 * Método 'excluirLivroTitulo' para buscar e excluir um livro através da busca pelo título do livro.

#### Classe ArquivoLivros 
  Foram realizadas alterações na classe 'create' para excluir as stopWord e adicionar palavras relevantes na lista invertida. Foi criado um método (linha 54) para receber palavras digitadas pelo usuário separadas por espaço e retornar uma lista de Livros proporcionada pela interseção de lista de palavras recebidas. Exemplificando: se o usuário buscar pelas palavras "memoria" e "estrela", a classe não retornará uma lista de livros mesmo que uma das palavras esteja na lista. Também foram feitos acréscimos nos métodos delete(linha 98 a 103) e update(linha 123 a 136).

#### Experiência do grupo
  A partir do cadastro de cada livro, o tratamento para remoção de letras com palavras acentuadas não está completa. Todas as tentativas de verificação e alteração de encoding não consegui deixar funcionando corretamente(diferentemente da disciplina de AED2 onde não encontrei este tipo de problema). Todas as palavras acentuadas retornaram um valor de 65533. Quanto a remoção de stopWords, estas foram devidamente retiradas durante o cadastro de um determinado livro e também retirados na consulta de livros por pesquisa por palavras chave.
Quanto a parte principal, que é o entendimento e utilização da lista invertida, não houve complicações ou problemas.

#### Perguntas objetivas sobre o projeto(chacklist):


* A inclusão de um livro acrescenta os termos do seu título à lista invertida?

  Não. Como dito anteriormente, houve apenas remoção de stopWords. Palavras cadastradas pelo sistema que contém acentos tem seus caracteres especiais removidos na inclusão da lista invertida, funcionando corretamente. Mas títulos com palavras com caracteres epeciais cadastradas pelo usuário, permanecerão acentuadas na lista invertida e para pesquisas devem ser feitas conforme cadastradas

* A alteração de um livro modifica a lista invertida removendo ou acrescentando termos do título?

  Sim, qualquer tipo de alteração do título de algum livro que tenha alteração no título tem suas palavras chave antigas excluídas da lista e as novas adicionadas.

* A remoção de um livro gera a remoção dos termos do seu título na lista invertida?
	Sim.

* Há uma busca por palavras que retorna os livros que possuam essas palavras?

  Sim. Mas como dito anteriormente, retorna a intercessão dos termos dos livros que possuam os termos pesquisados.
 
* Essa busca pode ser feita com mais de uma palavra?

  Sim, desde que estejam separadas por espaço.

* As stopwords foram removidas de todo o processo?

  Sim.

* Que modificação, se alguma, você fez para além dos requisitos mínimos desta tarefa?

  Não foi realizada nenhuma modificação extra.

* O trabalho está funcionando corretamente?

  Sim.
  
* O trabalho está completo?

  Não, por causa das palavras com caracteres especiais digitadas pelo usuário. Mesmo utilizando outros métodos, bibliotecas para leitura do teclado(BefferdReader) e verificando que todas as entradas estão na codificação "UTF-8", todo caracter especial é associado o valor 65533. Dessa forma, decidi manter a rotina feita originalmente apesar de não ter tanto eficiente quanto a solução apresentada.

* O trabalho é original e não a cópia de um trabalho de um colega?

  Sim, a classe e métodos criados e modificados foram realizados apenas pelo autor do projeto.




