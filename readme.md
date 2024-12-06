Projeto feito com os estudos feitos na Alura

Melhor usar a chave SSH

Chave SSH
Ao vincular um repositório remoto ao nosso repositório local, via comando git remote add, precisamos utilizar algum protocolo seguro, como HTTPS ou SSH. No caso de se utilizar o protocolo SSH, escolha realizada neste curso, devemos gerar uma chave SSH em nosso computador, além de cadastrá-la em nossa conta do GitHub. Isso é necessário para garantir a autenticação, pois o GitHub checa se quem está realizando o push dos commits tem permissão para realizar tal ação.

Geração de uma chave SSH
Antes de executar o comando git push, precisamos gerar uma chave SSH. A geração da chave é feita via terminal, com o comando ssh-keygen -t ed25519 -C "SEU EMAIL AQUI":

Cadastrando a chave SSH no GitHub
Após gerar a chave, precisamos cadastrá-la em nossa conta do GitHub, para que assim o GitHub consiga nos identificar e autenticar ao executar o comando git push de nosso computador.

Acesse a página de chaves SSH de sua conta no GitHub e clique no botão New SSH key ou Nova chave SSH para realizar o cadastro da chave:

Formulário para cadastro de chave SSH no site do GitHub, contendo os campos "title", "key type" e "key".

Repare que o formulário exibido na imagem anterior contém três campos:

Title ou Título: Informe um apelido para sua chave SSH (por exemplo: computador casa)
Key type ou Tipo de chave: Escolha o tipo Authentication Key ou Chave de autenticação
Key ou Chave: Nesse campo você deve colar o conteúdo do arquivo da sua chave SSH pública (arquivo id_ed25519.pub)
Após realizar esse procedimento, será possível sincronizar o repositório local com o remoto, enviando os novos commits com o comando git push.