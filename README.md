#Pesquisa Comparativa: XMLHttpRequest, Fetch, Promises e Async/Await
Este documento apresenta uma análise comparativa entre as quatro principais técnicas de requisições assíncronas no JavaScript: XMLHttpRequest, fetch, Promises e async/await. Cada uma dessas abordagens tem suas características, vantagens e desvantagens. Esta pesquisa tem como objetivo oferecer uma compreensão clara das diferenças entre elas, auxiliando na escolha da melhor solução para realizar requisições assíncronas.

#1. XMLHttpRequest
O XMLHttpRequest (XHR) é a API tradicional para realizar requisições HTTP assíncronas no JavaScript. Embora seja amplamente compatível com diversos navegadores, especialmente versões mais antigas, apresenta uma sintaxe complexa e limitações quanto à legibilidade e à organização do código.

Vantagens:
Compatibilidade: Funciona em todos os navegadores, incluindo versões mais antigas.

Controle Total: Permite um controle detalhado sobre a requisição, incluindo status, progresso e cabeçalhos HTTP.

Desvantagens:
Sintaxe Complexa: A utilização do XMLHttpRequest exige uma abordagem mais verbosa, dificultando a manutenção e legibilidade do código.

Callback Hell: O uso de callbacks torna o código difícil de ler, especialmente quando múltiplas requisições precisam ser encadeadas.

Erros Não Tratados: Não trata automaticamente erros HTTP, como status 404 ou 500.

#2. Fetch API
A fetch API é uma interface moderna e baseada em Promises para realizar requisições HTTP. Ela oferece uma sintaxe mais simples e limpa em comparação com XMLHttpRequest, facilitando o trabalho com requisições assíncronas.

Vantagens:
Sintaxe Simples: A fetch API usa Promises, tornando o código mais conciso e legível.

Suporte a Promises: Permite o encadeamento de requisições, facilitando a organização do código.

Tratamento Centralizado de Erros: Embora não trate automaticamente erros HTTP, a API permite a manipulação de erros de forma eficiente utilizando .catch().

Desvantagens:
Erros HTTP Não Tratados: A fetch não lança um erro para status HTTP de falha (como 404 ou 500). Erros são apenas tratados se ocorrerem na requisição ou na conversão de dados.

Sem Controle de Progresso: Não é possível monitorar o progresso da requisição, como em upload ou download de arquivos.

#3. Promises
As Promises são um padrão em JavaScript para trabalhar com operações assíncronas. Elas representam o valor de uma operação assíncrona que pode ser resolvido com sucesso ou com falha, permitindo que o código seja escrito de forma mais clara e legível.

Vantagens:
Encadeamento de Operações Assíncronas: As Promises permitem encadear múltiplas operações assíncronas sem a necessidade de callbacks, facilitando a organização do código.

Tratamento de Erros: O uso de .catch() permite tratar erros de forma centralizada e eficiente.

Desvantagens:
Complexidade com Múltiplas Promises: Embora facilite o encadeamento de operações, o código pode se tornar difícil de entender quando muitas Promises são encadeadas.

Não Resolve a Legibilidade: Quando comparada com async/await, o uso de várias Promises pode gerar código com múltiplos .then(), tornando-o menos legível.

#4. Async/Await
async/await é uma sintaxe moderna que facilita o trabalho com Promises, tornando o código assíncrono mais legível e parecendo com código síncrono. A sintaxe async/await é baseada em Promises, mas permite que a escrita do código seja mais fluida e compreensível.

Vantagens:
Sintaxe Legível: A principal vantagem do async/await é a clareza do código. Ele permite escrever código assíncrono de maneira que se assemelha a código síncrono.

Erros Tratados com Try/Catch: A manipulação de erros é feita de forma mais intuitiva, com o uso de try/catch.

Fluxo de Execução Claro: Com await, o código executa de forma sequencial, tornando mais fácil de entender a ordem das operações assíncronas.

Desvantagens:
Requer Suporte a ES2017+: A sintaxe async/await só é compatível com versões modernas do JavaScript, sendo necessária uma transpilação para navegadores mais antigos (como o Internet Explorer).

Necessita de Função async: A utilização do await só é possível dentro de uma função async, o que pode exigir mudanças na estrutura do código.
