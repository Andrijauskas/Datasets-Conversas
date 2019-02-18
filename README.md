# Datasets-Conversas

Repositório de datasets de conversas. Resultado da Iniciação Tecnológica da Adriana Andrijauskas intitulada "Desenvolvimento de Dataset e Base de Dados em Língua Portuguesa sobre Crimes Sexuais", realizada no Centro Universitário FEI, em 2018, com a orientação do professor doutor Rodrigo Filev Maia.

## Datasets
Neste trabalho é entendido como conversa culpada, aquela com grande suspeita da existência de um predador sexual. Por sua vez, uma conversa inocente é caracterizada pela não existência de um predador sexual, podendo ou não ser de cunho sexual.

Nenhum tipo de decreto judicial foi utilizado para a construção deste trabalho.
* c_pr: Conversas culpadas privadas, originalmente em formato de texto em arquivos TXT, geradas por comunicação virtual. 43 conversas e 14756 linhas. Conversas fornecidas através da parceria da FEI com o Ministério Público Federal (Adriana Shimabukuro). Tais conversas sofreram aplicação de restrições para a garantia de confidencialidade dos envolvidos, onde foram manipuladas, desde sua criação até sua finalização, em uma máquina localizada na sede do Ministério Público Federal – São Paulo. Mais informações referentes ao ocultamento de dados serão detalhadas abaixo;
* c_pu: Conversas culpadas públicas, originalmente em formato de texto em folhas impressas (print de tela de celular, foto de tela de celular, print de tela de computador ou foto de tela de computador), geradas por comunicação virtual. 39 conversas e 1824 linhas. Conversas foram fornecidas e sofreram a aplicação das mesmas restrições citadas acima;
* c_pu_mod: Conversas culpadas públicas modificadas. Baseado no arquivo c_pu, erros de português foram corrigidos através de modificações de concordância e interpretação de texto. Dimensões foram mantidas;
* i_pu: Conversas inocentes públicas, originalmente em formato de áudio e posteriormente transcritas em arquivos TXT, geradas por comunicação oral. 87912 linhas e 137 conversas. Conversas fornecidas através da parceria da FEI com a Universidade Federal de Minas Gerais (professora Heliana Ribeiro de Mello). 

## Restrições
Informações referentes à identificação ou localização os autores foram substituídas por termos associados, listados abaixo, para a garantia de confidencialidade dos envolvidos.
* \>audio< substitui arquivo de áudio;
* \>emoticon< substitui emoticons que seriam desformatados ao serem populados no dataset (exemplo: ☺), sem modificar emoticons compostos por caracteres (ex: =]);
* \>foto< substitui arquivos de imagem;
* \>local< substitui local de uma cidade, cidade, estado, país ou nacionalidade;
* \>nome< substitui nome ou apelido de autores;
* \>telefone< substitui número de contato.

## Estrutura
Todos os datasets possuem a mesma estrutura, descrita e exemplificada abaixo.

A estrutura da base de dados do PAN, referente à tarefa proposta em 2012 (https://www.uni-weimar.de/medien/webis/events/pan-12/pan12-web/author-identification.html), foi utilizada como referência.

Descrição da estrutura:

    <banco>
       <conversa id=“Número da conversa”>
          <linha num=“Número da linha”>
             <autor>Nome do autor criptografado em MD5</autor>
             <mensagem>Mensagem</mensagem>
          </linha>
          
          …
          
          <linha num=“Número da linha”>
             <autor>Nome do autor criptografado em MD5</autor>
             <mensagem>Mensagem</mensagem>
          </linha>
       </conversa>
       
       …
       
       <conversa id=“Número da conversa”>
          <linha num=“Número da linha”>
             <autor>Nome do autor criptografado em MD5</autor>
             <mensagem>Mensagem</mensagem>
          </linha>
          
          …
          
          <linha num=“Número da linha”>
             <autor>Nome do autor criptografado em MD5</autor>
             <mensagem>Mensagem</mensagem>
          </linha>
       </conversa>
    </banco>

Exemplo de preenchimento da estrutura:

    <banco>
       <conversa id=“1”>
          <linha num=“1”>
             <autor>709916bfe16ef8cdd6102dc5453f302f</autor>
             <mensagem>Voce deita com migo na cama pelada</mensagem>
          </linha>
          
          …
          
          <linha num=“5”>
             <autor>13f27f55ef3622f4e987aac6a57b1ce8</autor>
             <mensagem>Tah</mensagem>
          </linha>
       </conversa>
       
       …
       
       <conversa id=“39”>
          <linha num=“1”>
             <autor>884d8e4b677d1e6a6a731460b54032c3</autor>
             <mensagem>com meus pais, por q?</mensagem>
          </linha>
          
          …
          
          <linha num=“8”>
             <autor>2cd791880f8099210bfd6a79a16e4a53</autor>
             <mensagem>mas nao sou obrigada a agaraadar otdos</mensagem>
          </linha>
       </conversa>  
    </banco>
    
