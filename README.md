# Backup-de-switches-com-Python
Faz backup de switches Cisco e envia email informando se houve erros ou não.

O programa acessa os switches via SSH e executa o comando para enviar as configurações para um servidor de TFTP, depois envia um email informando se o backup foi finalizado corretamente ou se ocorreram falhas.

Foi gerado um arquivo .exe, na mesma pasta onde ficará o executável deve estar o arquivo texto com o nome dos switches e os 2 GIFS que serão inseridos no email. Usei o comando: " pyinstaller --onefile program.py " para gerar o executável, o parâmetro '--onefile' permite criar um executável sem qualquer outra dependência.

Atentar para o arquivo texto, não pode ter espaços em branco após cada linha e principalmente após a última linha, antes de salvar o arquivo, verifique se o cursor está posicionado logo após o último caracter da última linha (tive bastante problema com isso até descobrir q havia pressionado o ENTER no final da última linha.

Como no programa tem que colocar o usuário e senha para acessar os switches, criei um usuário nos switches com permissão somente para executar o comando 'show running config'.

O programa foi copiado para um servidor e adicionado no task scheduler para rodar semanalmente.
