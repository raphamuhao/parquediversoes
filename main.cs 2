using System;
using System.IO;
using System.Text; 
class MainClass {

  public static void Main (string[] args) { 
    int sair = 1;
    int  entradaUsuario = 0; 
    int entradaV = 0;
    bool verificaResposta;
    string entrada = null;
    Console.WriteLine("## Bem Vindo ao Parque ##");
    
    while(sair != 0 ){
      Console.WriteLine("## Digite o campo que deseja acessar na bilheteria ##"); 
      Console.WriteLine("## 1 - Ingresso ##");  
      Console.WriteLine("## 2 - Parque ##");
      Console.WriteLine("## 0 - Finalizar Programa ##");  
      entrada = Console.ReadLine();
      verificaResposta = digitosCertosUmDois(entrada) ;//TRATAR ENTRADA

      if(verificaResposta == false ){
       sair= 1;  
      }else{
        entradaUsuario = int.Parse(entrada);
        switch (entradaUsuario){
          //INGRESSO
          case 1:
            int entradaIngresso = 0;
            while(entradaIngresso >= 0 && entradaIngresso<= 2  ){
              verificaResposta = false;
              while(verificaResposta != true){
                Console.Clear();
                Console.WriteLine("## Escolha uma opção abaixo ##"); 
                Console.WriteLine("## 1 - Comprar ingresso ##"); 
                Console.WriteLine("## 2 - Consultar ingresso ##"); 
                Console.WriteLine("## 0 - Voltar menu inicial ##");
                entrada = Console.ReadLine();
                verificaResposta = digitosCertosUmDois(entrada);
                Console.Clear();
              }
              entradaIngresso = int.Parse(entrada);
              switch (entradaIngresso){
                //COMPRAR
                case 1:
                  Console.Clear();
                  Ingresso.cadastrarIngresso();
                  System.Threading.Thread.Sleep(TimeSpan.FromSeconds(3));  
                break;
                //CONSULTAR
                case 2:
                  verificaResposta = false;
                  while(verificaResposta != true){
                    int nuIngresso = 0;
                    Console.WriteLine( "## Informe número do ingresso: ##");
                    nuIngresso = int.Parse(Console.ReadLine());
                    Ingresso.consultarIngresso(nuIngresso);
                    verificaResposta = true;
                    while(verificaResposta !=false  ){
                      Console.WriteLine("## Deseja consultar outro ingresso? ##"); 
                      Console.WriteLine("## 1 - Sim ##"); 
                      Console.WriteLine("## 0 - VOLTAR MENU INICIAL  ##"); 
                      entrada = Console.ReadLine();
                      verificaResposta = digitosCertosZeroUm(entrada);
                      entradaUsuario = int.Parse(entrada);
                      if(entradaUsuario == 1){
                        Console.WriteLine( "## Informe número do ingresso: ##");
                        nuIngresso = int.Parse(Console.ReadLine());
                        Ingresso.consultarIngresso(nuIngresso);// MÉTODO CLASSE INGRESSO
                      }else{
                        verificaResposta = false;
                      }    
                    }
                    System.Threading.Thread.Sleep(TimeSpan.FromSeconds(3));
                    Console.Clear();
                    verificaResposta = true;
                  }
                  Console.Clear();  
                break;
                //VOLTAR MENU INICIAL
                case 3 :
                 entradaIngresso = 0;
                 verificaResposta = true;
                break;
                default:
                  Console.WriteLine("## VOLTANDO AO MENU INICIAL ##");
                  System.Threading.Thread.Sleep(TimeSpan.FromSeconds(3));
                  entradaIngresso = 0;
                  verificaResposta = true;
                  
                break;
              }
            }
          break;
          //PARQUE
          case 2:
            int entradaCliente = 0;
            while(entradaCliente >= 0 && entradaCliente <= 2  ){
              verificaResposta = false;
              while(verificaResposta != true){
                Console.Clear();
                Console.WriteLine("## Digite o número referente ao campo que quer acessar ##"); 
                Console.WriteLine("## 1 - ADMINISTRATIVO ##"); 
                Console.WriteLine("## 2 - BRINQUEDOS ##"); 
                Console.WriteLine("## 0 - Voltar menu inicial ##"); 
                entrada = Console.ReadLine();
                verificaResposta = digitosCertosUmDois(entrada);
                Console.Clear();
              }
              entradaCliente= int.Parse(entrada);
              switch (entradaCliente){
                //ADMINSTRATIVO
                case 1:
                 verificaResposta = false;
                  while(verificaResposta != true){
                    Console.WriteLine("## Digite o número referente ao campo que quer acessar ##"); 
                    Console.WriteLine("## 1 - CADASTRO DE FUNCIONARIOS ##");
                    Console.WriteLine("## 2 - FINANCEIRO ##");
                    Console.WriteLine("## 0 - Voltar menu inicial ##"); 
                    entrada = Console.ReadLine();
                    verificaResposta = digitosCertos(entrada);
                    entradaUsuario = int.Parse(entrada);
                    
                    Console.Clear();
                    switch(entradaUsuario){
                      case 1 :
                        while(entradaUsuario == 1){
                               
                        entradaUsuario = int.Parse(entrada);
                        
                        if(verificaResposta == false){
       			              sair = 1;  
     			              }else{
                          Funcionario.cadastrarFuncionario();
                          System.Threading.Thread.Sleep(TimeSpan.FromSeconds(3));                      

                        }
                        }

                      break;
                      case 2 :
                       Console.WriteLine("## Digite o numero referente ao campo que quer acessar ##"); 
                       Console.WriteLine("## 1 - Relátorio Saldo  ##");
                       Console.WriteLine("## 2 - Alterar Valor ingresso ##");
                       Console.WriteLine("## 0 - Voltar menu inicial ##"); 
                       entrada = Console.ReadLine();
                       verificaResposta = digitosCertos(entrada);
                       entradaUsuario = int.Parse(entrada);
                       Console.Clear();
                        switch(entradaUsuario){
                          case 1 :
                            Console.WriteLine("## De novo ##");
                            Console.WriteLine("## Informe tipo de Ingresso ##"); 
                            entrada = Console.ReadLine();
                            verificaResposta = digitosCertos(entrada);
                            entradaUsuario = int.Parse(entrada);
                            Ingresso.quantiVendida(entradaUsuario);
                            
                          break;
                          case 2 :
                            Console.WriteLine("## Informe qual tipo de ingresso deseja alterar : ##");  
                            Console.WriteLine("## 1 - Basico, 2 - Premium ou 0 para sair ##");  
                            entrada = Console.ReadLine();
                            verificaResposta = digitosCertos(entrada);
                            entradaV = int.Parse(entrada);
                            
                            if(entradaUsuario == 1){
                              Ingresso alterarIngresso = new Ingresso(entradaV);
                              Console.WriteLine("## Valor Atual Ingresso Premium: ##", alterarIngresso.getValorB());
                              Console.WriteLine("## Informe novo valor ##");
                              entrada = Console.ReadLine();
                              entradaV = int.Parse(entrada);
                              alterarIngresso.setValorB(entradaV);

                            }else{
                              Ingresso alterarIngresso = new Ingresso(entradaV);
                              if(entradaUsuario == 2){
                              Console.WriteLine("## Valor Atual Ingresso Premium: ##",alterarIngresso.getValorP());
                              Console.WriteLine("## Informe novo valor ##");
                              entrada = Console.ReadLine();
                              entradaV = int.Parse(entrada);
                              alterarIngresso.setValorP(entradaV);
                              }else{
                              verificaResposta = false;
                            }
                          }

                        break;
                        default:
                          verificaResposta = false;
                          entradaUsuario = 0;
                        break;
                      }  
                      break;
                      default:

                      break;
                    }
                  }
                break;
                //BRINQUEDO
                case 2: 
                  verificaResposta = false;
                  while(verificaResposta != true){
                    Console.WriteLine( "## INFORMAÇÕES ##"); 
                    Console.WriteLine( "## 1 - INFORMAÇÕES TÉCNICAS ##");
                    Console.WriteLine( "## 2 - CADASTRAR BRINQUEDO ##");
                    Console.WriteLine( "## 3 - EXIBIR LISTA USUÁRIOS ##");
                    Console.WriteLine( "## 4 - EXIBIR LISTA DE BRINQUEDOS POR TIPO DE INGRESSO ##");
                    Console.WriteLine( "## 5 - VALIDAR INGRESSO ##");
                    Console.WriteLine( "## 0 - Voltar menu inicial ##");
                    entrada = Console.ReadLine();
                    verificaResposta = digitosCertosUmAoCinco(entrada);
                    Console.Clear();
                  }
                  Console.Clear(); 
                break;
                //VOLTAR MENU INICIAL
                case 3:
                  entradaCliente = 1; 
                break;
                default:
                  Console.WriteLine("## Opção inválida ##");
                  System.Threading.Thread.Sleep(TimeSpan.FromSeconds(3));
                  entradaCliente = 0;
                  
                break;
              }
            }
          break;
          case 3:
           sair = 0;
          break;
          default:
            sair = 0;
          break;
          
          
        }
      }
    }
  }
 
  //FUNÇAO TRATAR ENTRADA INICIAL(0,1,3) 
  public static bool digitosCertos(string entrada){
    char primeiroCaracter = entrada[0];
    int codigoAscii = Convert.ToInt32(primeiroCaracter );
    if(codigoAscii < 48 || codigoAscii > 51 || entrada.Length > 1){
      Console.WriteLine("Opção inválida");
      Console.WriteLine("Digite uma opção correta ou 0 prar sair");
      System.Threading.Thread.Sleep(TimeSpan.FromSeconds(4));
      Console.Clear();
      return false;
    }
    
    return true;  
  }
  //FUNÇAO TRATAR ENTRADA NUMERO 0,1,2.
  public static bool digitosCertosUmDois(string entrada){
    char primeiroCaracter = entrada[0];
    int codigoAscii = Convert.ToInt32(primeiroCaracter);
    if(codigoAscii < 27 || codigoAscii > 51 || entrada.Length > 1){
      Console.WriteLine("Opção inválida");
      Console.WriteLine("Digite uma opção correta ou 0 prar sair");
      System.Threading.Thread.Sleep(TimeSpan.FromSeconds(3));
      return false;   
    }
    return true;  
  }
 //FUNÇAO TRATAR ENTRADA NUMERO 1 E 0
  public static bool digitosCertosZeroUm(string entrada){
    char primeiroCaracter = entrada[0];
    int codigoAscii = Convert.ToInt32(primeiroCaracter );
    if(codigoAscii < 47 || codigoAscii > 50 || entrada.Length > 1){
      Console.WriteLine("Opção inválida");
      Console.WriteLine("Digite uma opção correta ou 0 prar sair");
      System.Threading.Thread.Sleep(TimeSpan.FromSeconds(2));
      return false;
      
    }
    return true;  
  }
  
  //FUNÇAO TRATAR ENTRADA NUMERO CADASTRO
  public static bool digitosCertosNumeroQualquer(string entrada){
    char primeiroCaracter = entrada[0];
    int codigoAscii = Convert.ToInt32(primeiroCaracter );
    if(codigoAscii < 47 || codigoAscii > 57 || entrada.Length > 1){
      Console.WriteLine("Opção inválida");
      Console.WriteLine("Digite uma opção correta ou 0 prar sair");
      System.Threading.Thread.Sleep(TimeSpan.FromSeconds(3));
      return false;  
    }
    return true;  
  }

    //nova função para tratar entrada do brinquedo
    public static bool digitosCertosUmAoCinco(string entrada){
    char primeiroCaracter = entrada[0];
    int codigoAscii = Convert.ToInt32(primeiroCaracter );
    if(codigoAscii < 47 || codigoAscii > 57 || entrada.Length > 5){
      Console.WriteLine("Opção inválida");
      Console.WriteLine("Digite uma opção correta ou 0 prar sair");
      System.Threading.Thread.Sleep(TimeSpan.FromSeconds(3));
      return false;  
    }
    return true;  
  }

}
