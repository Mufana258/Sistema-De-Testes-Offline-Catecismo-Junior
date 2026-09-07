# Sistema de Testes Offline — Catecismo Júnior

Aplicação autónoma para o professor criar e aplicar testes de escolha múltipla
sem internet. O programa funciona num único ficheiro `index.html`, com HTML,
CSS e JavaScript incorporados. Não é necessário instalar dependências, criar
uma conta ou utilizar um serviço online.

## Conteúdo do pacote

O pacote final contém apenas:

- `index.html` — aplicação completa para o professor e para o aluno;
- `README.md` — estas instruções.

Não são necessários `package.json`, Node.js, servidor de desenvolvimento ou
ficheiros de configuração.

## Como iniciar

1. Extraia o ZIP para o computador, tablet ou telemóvel do professor.
2. Abra o ficheiro `index.html` no navegador.
3. Não altere o nome do ficheiro: ele é a aplicação principal.
4. Pode abrir o ficheiro diretamente, sem internet.

O navegador pode mostrar um aviso de segurança ao abrir ficheiros locais. É
normal: escolha a opção para abrir o ficheiro no navegador.

## Criar um teste

No **Modo Professor**:

1. Escreva o nome do teste.
2. Edite as perguntas de demonstração ou elimine-as.
3. Use **Adicionar pergunta** para criar perguntas novas.
4. Escreva o texto da pergunta.
5. Adicione entre **1 e 4 opções** de resposta.
6. Marque o botão circular da opção correta.
7. Repita até um máximo de **20 perguntas**.
8. Use **Fazer Teste Agora** para testar no mesmo dispositivo ou escolha
   **Descarregar Teste do Aluno (.html)** para gerar um ficheiro independente.

As perguntas sem texto ou sem opções preenchidas são ignoradas quando o teste
é gerado. O resultado é calculado apenas com as perguntas válidas existentes:
por exemplo, 16 respostas certas em 17 perguntas válidas correspondem a
`16/17`.

O nome do teste é utilizado no nome do ficheiro descarregado. O ficheiro
gerado pelo botão **Descarregar Teste do Aluno (.html)** inclui as perguntas,
as respostas certas, o estilo, a leitura de acessibilidade e o gerador de
código QR. Pode ser aberto sozinho, sem outros ficheiros.

## Aplicar o teste aos alunos

Para vários dispositivos, o professor pode:

1. criar o teste no seu dispositivo;
2. descarregar o ficheiro HTML do teste;
3. criar um hotspot/rede local;
4. disponibilizar o ficheiro através de uma aplicação gratuita de servidor
   HTTP local, disponível na App Store ou no Google Play Store;
5. indicar aos alunos o endereço local para abrirem o teste no navegador.

Esta aplicação não cria o hotspot nem o servidor HTTP. Esses recursos são
fornecidos pelo sistema operativo ou pela aplicação de servidor local
escolhida pelo professor. A utilização de até 15 alunos em simultâneo
depende da capacidade do dispositivo, da rede local e da aplicação usada.

## Como o aluno responde

O aluno escreve o nome e inicia o teste. O modo de resposta foi pensado para
ser utilizado com toques:

- toque **1** para escolher a opção 1;
- toque **2** para escolher a opção 2;
- toque **3** para escolher a opção 3;
- toque **4** para escolher a opção 4, quando existir;
- depois de aproximadamente 3 segundos, a resposta fica bloqueada e o teste
  avança;
- **6 toques** no ecrã regressam à primeira pergunta para revisão;
- **7 toques** mantêm a resposta guardada da pergunta atual e avançam sem a
  alterar.

Também é possível usar as teclas numéricas `1` a `4`, `6` e `7` num
computador. O botão **Anterior** permite voltar uma pergunta durante a
revisão.

No modo de teste, a leitura em voz alta não lê a pergunta nem as opções
selecionadas. A aplicação apenas confirma por áudio que a questão ficou
**bloqueada**, evitando que a resposta seja anunciada à turma. Os botões,
campos e instruções de navegação podem ser lidos pelo navegador. O botão
**Voz** permite ligar ou desligar esta funcionalidade.

## Resultados e código QR

Quando todas as perguntas forem respondidas:

1. entregue o dispositivo ao professor;
2. o professor escolhe **Gerar Código QR com Correção**;
3. a aplicação apresenta a pontuação, a percentagem e as perguntas erradas;
4. é gerado um código QR local com o nome do aluno, o nome do teste, a
   pontuação e o detalhe das respostas.

O QR é criado no próprio dispositivo. Não é enviado para a internet e não
depende de uma conta ou de um serviço externo. O texto do QR também fica
visível no ecrã e pode ser copiado manualmente.

## Acessibilidade e inclusão

- interface de alto contraste;
- texto e botões grandes;
- leitura em voz alta dos controlos;
- confirmação sonora quando uma resposta fica bloqueada;
- navegação por teclado em computadores;
- funcionamento offline depois de o ficheiro estar disponível no dispositivo;
- revisão das respostas sem obrigar o aluno a começar de novo.

## Guardar ou reutilizar perguntas

O botão **Exportar Perguntas (JSON)** guarda as perguntas num ficheiro de
backup. O botão **Importar Teste (JSON/HTML)** permite carregar novamente um
backup ou um teste HTML criado pela aplicação. Estes ficheiros são opcionais:
o funcionamento normal requer apenas o `index.html` principal e, para cada
turma, o ficheiro HTML do teste descarregado.

## Privacidade e dependências

O pacote final não contém chamadas de rede, publicidade, telemetria ou
metadados de ferramentas de desenvolvimento. Toda a lógica necessária para
criar testes, aplicar perguntas, corrigir respostas e gerar QR está incorporada
no `index.html`.

Para manter o funcionamento offline, não substitua o conteúdo do ficheiro
principal por uma página que dependa de scripts externos. Se o teste for
partilhado por uma rede local, utilize apenas o endereço local fornecido pelo
servidor HTTP do professor.

## Contribuição

Este projeto está aberto à colaboração de programadores, designers,
profissionais de UX/UI, especialistas em acessibilidade, igrejas, catequistas,
professores e outras pessoas que possam contribuir para a sua evolução.

O objetivo é melhorar uma ferramenta simples para criar e aplicar testes do
Catecismo Júnior offline. A aplicação principal é um `index.html` autónomo:
permite ao professor criar entre 1 e 20 perguntas, definir entre 1 e 4 opções
por pergunta, marcar as respostas corretas, descarregar o teste do aluno,
acompanhar a revisão por toques e gerar o resultado com código QR sem
internet.

Todas as contribuições devem preservar o objetivo principal: uma ferramenta
simples, acessível, privada e utilizável offline por professores e alunos.

As contribuições não devem:

- transformar a aplicação numa página dependente de internet;
- adicionar rastreio, publicidade ou recolha de dados dos alunos;
- remover as funcionalidades de acessibilidade sem uma alternativa;
- substituir a aplicação autónoma por dependências externas obrigatórias;
- alterar o limite, a lógica de correção ou o modo de revisão sem documentar
  essa mudança.