class ContaBancaria:
    # Esta é a definição da classe ContaBancaria, que modela uma conta bancária.
    def __init__(self, nome):
        # Este é o método construtor que inicializa uma nova instância da classe.
        self.nome = nome  # Atribui o nome do titular da conta ao atributo 'nome'.
        self.saldo = 0  # Inicializa o saldo da conta como 0.
        self.depositos = []  # Cria uma lista vazia para armazenar os depósitos.
        self.saques = []  # Cria uma lista vazia para armazenar os saques.

    def depositar(self, valor):
        # Método para depositar dinheiro na conta.
        if valor > 0:
            # Verifica se o valor do depósito é positivo.
            self.saldo += valor  # Adiciona o valor ao saldo.
            self.depositos.append(valor)  # Registra o depósito na lista.
            # Imprime uma mensagem de confirmação com o valor depositado e o saldo atual.
        else:
            # Se o valor não for positivo, imprime uma mensagem de erro.
    
    # Os métodos 'sacar' e 'extrato' seguem uma lógica similar ao método 'depositar'.
class SistemaBancario:
    # Esta é a definição da classe SistemaBancario, que gerencia a conta bancária.
    def __init__(self):
        self.conta = None  # Inicializa a conta como None.

    def iniciar_sistema(self):
        # Método para iniciar o sistema bancário.
        nome_usuario = input("Digite o nome do usuário: ")  # Pede o nome do usuário.
        self.conta = ContaBancaria(nome_usuario)  # Cria uma nova conta bancária com o nome do usuário.

        while True:
            # Loop infinito para o menu de opções.
            # Imprime as opções disponíveis no sistema.
            opcao = int(input("Escolha uma opção: "))  # Pede ao usuário para escolher uma opção.

            # Condicional para executar a ação correspondente à opção escolhida.
            # Se a opção for 4, o loop é interrompido e o sistema é encerrado.
            # Se a opção não for válida, uma mensagem de erro é impressa.
if __name__ == "__main__":
    # Este bloco é executado se o script for o programa principal.
    sistema = SistemaBancario()  # Cria uma instância do sistema bancário.
    sistema.iniciar_sistema()  # Inicia o sistema bancário.
