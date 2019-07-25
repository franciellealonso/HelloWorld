# HelloWorld
Meu primeiro repositório
lista = ["Francielle" , "Leila" , "Luciano"]
senhas = ["Francielle" , "Leila" , "Luciano"]
while True:
  
  print("-= Sistema da Fran =- \n")
    
  print("1. Cadastro de usuários")
  print("2. Listagem de usuários")
  print("3. Deletar usuários")
  print("4. Acessar Sistema")
  print("5. Sair do Sistema")
  
  opcao= input("Digite a opção desejada: ")
  
  if opcao == "1":
    usuario= input("Cadastre usuário: ")
    lista.append(usuario)
    senha= input("Cadastre sua senha: ")
    senhas.append(senha)
    print("Usuário Cadastrado com sucesso!")
  elif opcao == "2":
    for u in lista:
      print(lista.index(u), " - ",u)
  elif opcao == "3":
    usuario = input("Digite o nome do usuário que deseja deletar: ")
    pos = lista.index(usuario)
    del senhas[pos]
    del lista[pos]
    print("{0}, foi deletado da lista".format(usuario))
  elif opcao == "4":
    loginus= input("Usário: ")
    senhaus= input("Senha: ")
    for u in lista:
      if u == loginus:
        pos = lista.index(u)
        if senhaus == senhas[pos]:
          print("{0}, Seja bem vindo(a)!".format(loginus))
          break
        else:
          print("Senha inválida!")
    else:
      print("Usuário não encontrado")
  elif opcao == "5":
    print("Sistema desconectado!")
    break  
