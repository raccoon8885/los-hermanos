# Especificação do Sistema Web para Recomendação de Filmes, Séries e Livros - Compass


**Índice**

- [1. Introdução](#1-introdução)
- [2. Escopo do projeto](#3-escopo-do-projeto)
- [3. Interessados](#4-interessados)

# 1. Introdução
Este documento visa a especificação de requisitos para o sistema Compass, o qual o principal objetivo é a recomendação 
de filmes, séries e livros pelos usuários cadastrados, promovendo o engajamento social através comentários, sugestões, 
avaliações e interações. Deste modo, o sistema servirá como uma especie de rede social, para que membros possam 
compartilhar seus interesses e descobrir novas opções de entreterimento e pessoas que partilham dos mesmos interesses. 

# 2. Escopo do projeto
O escopo do projeto é um sistema web de recomendação de filmes, séries e livros, com um viés de rede social, o qual os 
usuários poderam interagir entre si, com um design responsivo e leve, podendo ser acessado através de qualquer navegador,
seja por um dispostivo movél ou desktop. 

O sistema web será desenvolvido em python, HTML e CSS, terá seus dados persistidos por um banco de dados relacional e será implementado por um provedor de serviços da internet em nuvém. Em relação a segurança do site, o usuário sera protegido por uma senha, criada pelo próprio, a qual sera armazenda de modo criptografada em nosso banco de dados. 

# 3. Interessados
Aqueles que irão se beneficiar diretamente e aqueles que serão afetados pelo novo sistema:

Clientes: Conseguirão navegar pelo site para comentar, sugerir e avaliar filmes, séries e livros, além de interagir com
outros usuários da plataforma sobre os conteudos postados. 

Desenvolvedores: Seram responsável pela criação do sistema, do Front-End até o Back-End. Garantindo a melhor experiência possivel para o usuário. 

Criadores de conteúdo: Poderam acessar as avaliações, comentários e críticas sobre os conteudos discutidos pelos usuários na plataforma. 

# 4. Objetos funcionais

a. O sistema deverá permitir que os usuários criem e entrem com uma conta própria cadastrada com nome de usuário e senha.

Isso permitirá que cada um escreva sua própria avaliação.
Além disso, permitirá que os moderadores e administradores da página saibam quem pode estar cometendo algum tipo de conduta proibida na plataforma e tomar as atitudes necessárias.

b. O sistema deverá permitir que os usuários encontrem títulos de filmes, séries e livros assim como seu ano de lançamento, sinopse, gênero, duração, direção e elenco principal.

c. O sistema deverá permitir que usuários acessem e escrevam avaliações de filmes, séries e livros.

Para os clientes, isto facilitará na hora de escolher ou adquirir algum título de acordo com a avaliação lida.
E para os geradores dos conteúdos será uma boa forma de saber como o que foi produzido impactou os espectadores.

d. O sistema permitirá que os usuários alterem ou excluam suas próprias avaliações.

e. O sistema deverá permitir que usuários adicionem títulos na plataforma, sob aprovação dos administradores.

f. O sistema deverá permitir que os usuários configurem seu perfil como público ou privado.

g. O sistema deverá permitir que os usuários acessem perfis de outros usuários para visualizar as avaliações feitas, sob configuração de privacidade do perfil.

h. O sistema deverá permitir que usuários possam compartilhar títulos ou avaliações via link.


#  5. Objetos não-funcionais 
a. O sistema deverá funcionar em qualquer navegador(ex chrome, firefox e etc) 

b. O sistema deve funcionar 100% online. 

c. O sistema terá aplicativo, será apenas acessado pelo navegador.

d. O sistema web será desenvolvido em Python, Java e CSS.

e. O número de páginas web pelas quais o usuário precisa navegar para acessar a informação de livros, filmes e séries será de no máximo 2.

f. O sistema deverá ser capaz de suportar 1000 usuários simultâneos.

g. O Sistema deverá carregar a página em no máximo 5  segundos.

h. O tempo médio para baixar e visualizar um whitepaper em uma conexão de 1Mbps não deverá exceder 10 segundos.

i. O sistema deverá oferecer acesso protegido por senha para páginas web que são acessadas somente por funcionários.

j. Os dados de transação devem ser transmitidos de forma criptografada.

k. O sistema não deve permitir que usuário cadastre o mesmo filme, livro e série .

 
l. O sistema deverá disponibilizar uma página web que explica como navegar pelo site. A página deverá ser customizada com base nas páginas que o usuário pode acessar. Esta página de ajuda deverá ser acessível a partir de todas as outras páginas.

m. O sistema deverá ter interface com
Uma base de dados relacional para informações do cliente.
Uma base de dados relacional para informações dos livros, filmes e séries.





