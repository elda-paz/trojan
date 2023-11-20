# Remote Control Python Backdoor

Este é um simples backdoor Python que permite controle remoto de uma máquina. O backdoor se conecta a um servidor de comando e controle (C2) especificado e executa comandos recebidos do C2 no sistema alvo. Ele também possui funcionalidades de persistência para garantir que seja executado sempre que a máquina for iniciada.

## Configuração

Antes de usar o backdoor, certifique-se de configurar corretamente as seguintes variáveis no código:

- `CCIP`: O endereço IP do servidor de comando e controle.
- `CCPORT`: A porta na qual o backdoor se conectará ao servidor de comando e controle.

## Funcionalidades

### Persistência

A função `autorun` garante que o backdoor seja executado sempre que a máquina for inicializada. Ela copia o arquivo executável para o diretório de inicialização do usuário.

### Conexão ao Servidor de Comando e Controle

A função `conn` é responsável por estabelecer uma conexão com o servidor de comando e controle. Se a conexão for bem-sucedida, a função retorna o socket do cliente.

### Execução de Comandos

A função `cmd` executa comandos no sistema e envia a saída de volta para o servidor de comando e controle através da conexão estabelecida.

### Interface do Cliente

A função `cli` gerencia a interação contínua com o servidor de comando e controle. Ela recebe comandos do servidor, executa-os e envia a saída de volta.

## Uso

1. Configure as variáveis `CCIP` e `CCPORT` no código.
2. Execute o backdoor na máquina alvo.
3. O backdoor estabelecerá uma conexão com o servidor de comando e controle.
4. A partir do servidor de comando e controle, envie comandos para a máquina alvo.

**Observação:** Este código é fornecido apenas para fins educacionais e de pesquisa. O uso indevido do código é estritamente proibido. O autor não é responsável por qualquer dano causado pelo uso inadequado deste código. Use por sua conta e risco.
