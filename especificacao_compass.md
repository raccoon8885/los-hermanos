# Especificação do Sistema Web para Recomendação de Filmes, Séries e Livros - Compass


**Índice**

- [1. Introdução](#1-introdução)
- [2. Escopo do projeto](#3-escopo-do-projeto)
- [3. Interessados](#4-interessados)
-[4.requisitos funcionais]


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

Adminstrador: Será responsável por validar e gerenciar o sistema. 

Criadores de conteúdo: Poderam acessar as avaliações, comentários e críticas sobre os conteudos discutidos pelos usuários na plataforma. 

# 4. Requisitos funcionais 

RF 1. O sistema deverá permitir que os usuários criem e entrem com uma conta própria cadastrada com nome de usuário e senha.

     Isso permitirá que cada um escreva sua própria avaliação.
     Além disso, permitirá que os moderadores e administradores da página saibam quem pode estar cometendo algum tipo de conduta proibida na plataforma e tomar as atitudes            necessárias.

RF 2. O sistema deverá permitir que os usuários encontrem títulos de filmes, séries e livros assim como seu ano de lançamento, sinopse, gênero, duração, direção e elenco              principal.

RF 3. O sistema deverá permitir que usuários acessem e escrevam avaliações de filmes, séries e livros.

     Para os clientes, isto facilitará na hora de escolher ou adquirir algum título de acordo com a avaliação lida.
     E para os geradores dos conteúdos será uma boa forma de saber como o que foi produzido impactou os espectadores.

RF 4. O sistema permitirá que os usuários alterem ou excluam suas próprias avaliações.

RF 5. O sistema deverá permitir que usuários adicionem títulos na plataforma, sob aprovação dos administradores.

RF 6. O sistema deverá permitir que os usuários configurem seu perfil como público ou privado.

RF 7. O sistema deverá permitir que os usuários acessem perfis de outros usuários para visualizar as avaliações feitas, sob configuração de privacidade do perfil.

RF 8. O sistema deverá permitir que usuários possam compartilhar títulos ou avaliações via link.


#  5. Requisitos não-funcionais 
RNF 1. O sistema deverá funcionar em qualquer navegador(ex chrome, firefox e etc) 

RNF 2. O sistema deve funcionar 100% online. 

RNF 3. O sistema terá aplicativo, será apenas acessado pelo navegador.

RNF 4. O sistema web será desenvolvido em Python, Java e CSS.

RNF 5. O número de páginas web pelas quais o usuário precisa navegar para acessar a informação de livros, filmes e séries será de no máximo 2.

RNF 6. O sistema deverá ser capaz de suportar 1000 usuários simultâneos.

RNF 7. O Sistema deverá carregar a página em no máximo 5  segundos.

RNF 8. O tempo médio para baixar e visualizar um whitepaper em uma conexão de 1Mbps não deverá exceder 10 segundos.

RNF 9. O sistema deverá oferecer acesso protegido por senha para páginas web que são acessadas somente por funcionários.

RNF 10. Os dados de transação devem ser transmitidos de forma criptografada.

RNF 11. O sistema não deve permitir que usuário cadastre o mesmo filme, livro e série .

 
RNF 12. O sistema deverá disponibilizar uma página web que explica como navegar pelo site. A página deverá ser customizada com base nas páginas que o usuário pode acessar. Esta página de ajuda deverá ser acessível a partir de todas as outras páginas.

RNF 13. O sistema deverá ter interface com
Uma base de dados relacional para informações do cliente.
Uma base de dados relacional para informações dos livros, filmes e séries.

#  6. Casos de uso

**6.1 - Cadastrar novo membro**

![image](https://user-images.githubusercontent.com/38226976/113227930-2501dd80-926a-11eb-9732-172cce7a1296.png)


**Objetivo:** Criar conta no sistema para usuário.

**Atores:** Membro não registrado e sistema.

**Pré-condições:** O ator inserir seus dados pessoais corretamente. (Nome completo, data de nascimento, país onde reside, nome de usuário e senha)

**Pós-condições:** Usuário acessa a conta pessoal criada.

**Fluxo principal:**

     1. O usuário decide se cadastrar no sistema.
     2. O sistema solicita os dados pessoais para realizar o cadastro.
     3. O usuário insere os dados.
     4. O sistema verifica que não existe um cadastro com aquele mesmo nome de usuário e cadastra o usuário.
          
**Fluxo alternativo:**

     Fluxo alternativo a.  
     
          1. O usuário decide se cadastrar no sistema.           
          2. O sistema solicita os dados pessoais para realizar o cadastro.
          3. Usuário insere algum dado incompatível com o campo.
          4. O sistema informa que não é possível inserir aquele tipo de dado.

     Fluxo alternativo b.

          1. O usuário decide se cadastrar no sistema.
          2. O sistema solicita os dados pessoais para realizar o cadastro.
          3. O usuário insere os dados.
          4. O sistema identifica que já existe um usuário com aquele nome de usuário inserido.
          5. Retorna ao passo 3 do fluxo principal e o sistema solicita que o usuário escolha outro nome de usuário.



**6.2 - Efetuar login**

![UseCaseDiagram4 certo](https://user-images.githubusercontent.com/61236154/113448534-66ad9800-93d2-11eb-8b6b-ceca8db3539e.jpg)


**Objetivo:** Usuário acessar o aplicativo com sua conta.

**Atores:** Usuário e sistema.

**Pré-condições:** Usuário ser cadastrado no sistema.

**Pós-condições:** Acessar a área do aplicativo para membros.

**Fluxo principal:**

     1. Usuário decide fazer login no sistema.
     2. Sistema solicita nome de usuário e senha.
     3. Usuário insere nome de usuário e senha.
     4. Sistema verifica dados inseridos.
     5. Usuário acessa a área do aplicativo para membros.

**Fluxo alternativo:**

     Fluxo alternativo a.

          1. Usuário decide fazer login no sistema.
          2. Sistema solicita nome de usuário e senha.
          3. Usuário insere nome de usuário e senha.
          4. Sistema identifica dados incorretos inseridos.
          5. Retorna ao passo 2 do fluxo principal.          

**6.3 - Avaliar título**
![UseCaseDiagram1](https://user-images.githubusercontent.com/61236154/113448548-74631d80-93d2-11eb-87ca-8408932b4795.jpg)


**Objetivo:** Inserir avaliação de título para que outros usuário possam ler.

**Atores:** Membro cadastrado, sistema e administrador.

**Pré-condições:** Usuário ter selecionado algum título no aplicativo para avaliar.

**Pós-condições:** Avaliação sob avaliação do administrador.

**Fluxo principal:**

     1. Usuário decide avaliar título.
     2. Usuário digita sua avaliação.
     3. Usuário submete sua avaliação.
     4. Sistema armazena avaliação.
     5. Sistema envia avaliação a administrador.
     6. Administrador aprova avaliação.
     7. Sistema deixa visível avaliação na página do título avaliado.
     8. Sistema notifica usuário.

**Fluxo alternativo:**

     Fluxo alternativo a.

          1. Usuário decide avaliar título.
          2. Usuário digita uma quantidade de caracteres maior que o permitido.
          3. Sistema informa que a avaliação está grande demais.
          4. Segue no passo 2 do fluxo principal.

     Fluxo alternativo b.

          1. Usuário decide avaliar título.
          2. Usuário digita sua avaliação.
          3. Usuário submete sua avaliação.
          4. Sistema armazena avaliação.
          5. Sistema envia avaliação a administrador.
          6. Administrador reprova avaliação do usuário sobre o título.
          7. Sistema notifica usuário.
          
**6.4 - Cadastrar título**

![UseCaseDiagram2](https://user-images.githubusercontent.com/61236154/113448582-82b13980-93d2-11eb-8a30-f598477675b1.jpg)



**Objetivo:** Inserir um título não existente ainda no sistema para que outros usuários possam visualizar e avaliar.

**Atores:** Membro, sistema e administrador.

**Pré-condições:** Estar logado no sistema.

**Pós-condições:** Título cadastrado no sistema.

**Fluxo principal:**

1.	Usuário decide cadastrar título.
2.	Sistema solicita dados do título. (Tipo, nome, gênero, duração, elenco, diretor e ano de lançamento)
3.	Usuário insere dados do título.
4.	Usuário submete dados do título.
5.	Sistema armazena dados e envia a administrador.
6.	Administrador aprova cadastro de título.
7.	Sistema notifica usuário.

**Fluxo alternativo:**

	Fluxo alternativo a.

1.	Usuário decide cadastrar título.
2.	Sistema solicita dados do título. (Tipo, nome, gênero, duração, elenco, diretor e ano de lançamento)
3.	Usuário insere dados do título.
4.	Sistema identifica dados incompatíveis com os campos.
5.	Retorna ao passo 2.

Fluxo alternativo b.

1.	Usuário decide cadastrar título.
2.	Sistema solicita dados do título. (Tipo, nome, gênero, duração, elenco, diretor e ano de lançamento)
3.	Usuário insere dados do título.
4.	Usuário submete dados do título.
5.	Sistema armazena dados e envia a administrador.
6.	Administrador reprova cadastro de título.
7.	Sistema notifica usuário.

**6.5 – Consultar relatórios**
![UseCaseDiagram3](https://user-images.githubusercontent.com/61236154/113448631-952b7300-93d2-11eb-88c6-07c7ede65bd9.jpg)


**Objetivo:** Manter administrador informado sobre ações e conteúdo no sistema.

**Atores:** Sistema e administrador.

**Pré-condições:** Administrador estar logado no sistema.

**Pós-condições:** Visualização de relatório gerado.

**Fluxo principal:**

1.	Administrador decide visualizar relatório.
2.	Administrador entra na página de gerente.
3.	Sistema gera relatórios.
4.	Sistema apresenta relatórios.

**Fluxo alternativo:** Não possui.

**6.6 – Adicionar usuário como amigo**

![UseCaseDiagram5](https://user-images.githubusercontent.com/61236154/113448655-9fe60800-93d2-11eb-9865-6541f8f1e331.jpg)


**Objetivo:** Saber de algumas ações no sistema do usuário ou manter contato com ele.

**Atores:** Membros e sistema.

**Pré-condições:** Acessar página do perfil do outro usuário e usuário ainda não serem amigos na rede.

**Pós-condições:** Adicionado outro usuário como amigo.

**Fluxo principal:**

     1.	Usuário decide adicionar outro membro como amigo.
     2.	Usuário submete solicitação de amizade para o outro membro.
     3.	Sistema envia a solicitação ao outro membro.
     4.	Outro membro aceita solicitação de amizade.
     5.	Sistema notifica membro que enviou solicitação.

**Fluxo alternativo:**

	Fluxo alternativo a.

          1.	Usuário decide adicionar outro membro como amigo.
          2.	Usuário submete solicitação de amizade para o outro membro.
          3.	Sistema envia a solicitação ao outro membro.
          4.	Outro membro recusa solicitação de amizade.

**6.7 – Pesquisar usuário**

![UsecaseDigrama 7](https://user-images.githubusercontent.com/61236154/113491034-37fff200-94a4-11eb-8cdb-dab61e147274.jpg)


**Objetivo:** Encontrar outros membros cadastrados.

**Atores:** Usuário e sistema.

**Pré-condições:** Estar logado no sistema.

**Pós-condições:** Visualizar resultados de pesquisa.

**Fluxo principal:**

1.	Usuário decide pesquisar outro membro cadastrado.
2.	Usuário digita pelo nome na barra de pesquisa.
3.	Sistema consulta nome como aquele digitado.
4.	Sistema apresenta resultados.

**Fluxo alternativo:**

	Fluxo alternativo a.

1.	Usuário decide pesquisar outro membro cadastrado.
2.	Usuário digita pelo nome na barra de pesquisa.
3.	Sistema consulta nome como aquele digitado.
4.	Sistema não encontra resultados.
5.	Sistema informa que não foram encontrados resultados.

**6.8 – Pesquisar título**

![UseCaseDiagram 8](https://user-images.githubusercontent.com/61236154/113491138-d4c28f80-94a4-11eb-8884-74c528e9b21c.jpg)

**Objetivo:** Encontrar títulos cadastrados.

**Atores:** Usuário e sistema.

**Pré-condições:** Estar logado no sistema.

**Pós-condições:** Visualizar resultados de pesquisa.

**Fluxo principal:**

1.	Usuário decide buscar por um título.
2.	Usuário digita na barra de pesquisa informação sobre o título.
3.	Sistema realiza busca por título contendo uma informação como aquela.
4.	Sistema exibe resultados.

**Fluxo alternativo:**

	Fluxo alternativo a.

1.	Usuário decide buscar por um título.
2.	Usuário digita na barra de pesquisa informação sobre o título.
3.	Sistema realiza busca por título contendo uma informação como aquela.
4.	Sistema não encontra resultado.
5.	Sistema informa que não foram encontrados resultados como aquele.

          
# 7. Diagrama de Sequência



   **1 Membro não castrado** 

![diagrama de sequencia membro não registrado5](https://user-images.githubusercontent.com/61236154/113491187-47336f80-94a5-11eb-8045-da90cc49bf08.jpeg)

   **2 Login**

![diagrama de sequencia fazer login 6](https://user-images.githubusercontent.com/61236154/113491223-806bdf80-94a5-11eb-83f8-e1cebd6915b2.jpeg)

   **3.1 AddFilme**

![Diagrama em branco addfilme2](https://user-images.githubusercontent.com/61236154/113491235-a1343500-94a5-11eb-881d-0eb7b800c9f9.jpeg)

   **3.2 AddSerie**

![Diagrama em branco addLivro2](https://user-images.githubusercontent.com/61236154/113491261-d6408780-94a5-11eb-9303-c0c109dfeed4.jpeg)

   **3.3 AddLivro**

![Diagrama em branco addLivro2](https://user-images.githubusercontent.com/61236154/113491270-dd679580-94a5-11eb-9582-ac3869d04ed5.jpeg)

   **4.1 Fazer avaliação**

![Diagrama em branco seuqencia avaliação](https://user-images.githubusercontent.com/61236154/113491315-30d9e380-94a6-11eb-826d-858ee7619230.jpeg)

   **4.2 Deixar like**

![Diagrama em branco sequencia avalia like](https://user-images.githubusercontent.com/61236154/113491331-4e0eb200-94a6-11eb-84a6-8914b1780893.jpeg)

   **5.1 Solicita Amigo**
![diagrama de sequencia solicita amigo1](https://user-images.githubusercontent.com/61236154/113491350-70083480-94a6-11eb-911c-3ab21c3fbbed.jpeg)

   **5.2 Aceita amigo**
![diagrama de sequencia addamigo1](https://user-images.githubusercontent.com/61236154/113491360-8615f500-94a6-11eb-8422-ddba4f9c7801.jpeg)

   **5.3 Rejeita amigo**

![amigo rejeitado1](https://user-images.githubusercontent.com/61236154/113491370-a04fd300-94a6-11eb-9994-5a6dfb2ed4ba.jpeg)

   **6 Gerente**

![diagrama de sequencia gerente 4](https://user-images.githubusercontent.com/61236154/113491385-c1182880-94a6-11eb-9ccd-cb5f611da6da.jpeg)

   **7 Pesquisa membro**
   
   ![Diagrama_pesquisar_membro](https://user-images.githubusercontent.com/61236154/113491658-ddb56000-94a8-11eb-8166-34d50bd4ac62.jpeg)

   **8 pesquisa titulo**
   
   ![Diagrama_pesquisar_titulo](https://user-images.githubusercontent.com/61236154/113491660-e6a63180-94a8-11eb-8b77-2fc3cbca118c.jpeg)


# 8. Diagrama de domínio
![diagramaDeDominio_R002](https://user-images.githubusercontent.com/61977035/113274722-628b5880-92b4-11eb-8bcf-d5b81c36d0f2.png)

# 9. Diagrama de Classes
![diagramaDeClasse_R002](https://user-images.githubusercontent.com/61977035/113002383-16bba080-9148-11eb-8ff8-023b447820cb.jpeg)

# 10. Wireframes


