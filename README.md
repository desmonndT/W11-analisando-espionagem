# W11-analisando-espionagem
Neste estudo, visamos analisar a possível espionagem no sistema operacional Windows, durante e após a instalação, por meio da captura de pacotes de rede em uma máquina virtual. Para alcançar esse objetivo, os seguintes passos foram seguidos:

1.Configuração da Infraestrutura
Configuração da MaquinaVirtual(VM): Inicialmente, foi escolhida uma máquina virtual como ambiente de teste. Foi utilizado o software de virtualização VirtualBox, permitindo a criação de uma máquina virtual dedicada ao Windows 11. Durante a etapa de instalaçao, a máquina estava conectada à rede, possibilitando a coleta de dados de rede. Configurou-se a interface de rede da VM para usar "Adaptador Ponte", garantindo a conectividade total à rede.
2.Configuração da Captura de Pacotes
Para capturar o tráfego de rede, o software Wireshark foi instalado no sistema host (Linux Mint). Com o Wireshark devidamente configurado, a captura de pacotes foi iniciada, assegurando que a interface de rede do adaptador ponte estivesse selecionada, para capturarmos somente o trafego da VM.
A instalação do Windows na máquina virtual foi iniciada. Durante esse processo, o Wireshark estava em execução, registrando o tráfego de rede em tempo real. A captura de pacotes foi encerrada após um período de aproximadamente 50 a 60 minutos, abrangendo tanto a instalação quanto o uso do sistema operacional Windows após a instalação.
Os resultados da captura foram salvos em um arquivo de registro para análise dos dados capturados.

RESULTADOS E CONCLUSÃO
O arquivo de trafego gerado ficou com 853,3MB de tamanho.
![image](https://github.com/desmonndT/W11-analisando-espionagem/assets/27284652/bb11a794-c8fd-456b-b330-7a6b21c0b2f5)

Ao todo, os hosts e/ou IP de destino somam 120 Ethernet, 337 IPv4, 68 IPv6, 992 TCP e 4237 UDP, um total de 5.754 pacotes de rede durante o processo de instalação e uso do Windows na máquina virtual.
![image](https://github.com/desmonndT/W11-analisando-espionagem/assets/27284652/2bb3ec4e-0107-4dd9-91ed-3c3a159a43ff)

Os mais usados foram:
 48:8f:5a:a:93:0f (Ethernet): esse endereço MAC foi responsável por enviar ou receber um total de 1.112.109 pacotes.
![image](https://github.com/desmonndT/W11-analisando-espionagem/assets/27284652/e0ab2c1b-b854-431a-ae78-12a66d45bea2)

O endereço IP 192.168.2.204 (IPv4) foi responsavel por  933.755 unidades de dados transmitidas ou recebidas por esse dispositivo específico.
![image](https://github.com/desmonndT/W11-analisando-espionagem/assets/27284652/c92855a8-9f11-493a-9e38-fd9827d902f5)

Na rede IPv6 foram capturados 2.024 pacotes no endereço ff02::c. 
![image](https://github.com/desmonndT/W11-analisando-espionagem/assets/27284652/5284cf96-1b6f-47c3-929d-b4299f5ea9d9)

No TCP foram o endereço 45.227.91.64 foi o que maior  enviou/recebeu, foram 361.117 pacotes. 
![image](https://github.com/desmonndT/W11-analisando-espionagem/assets/27284652/ed52ec30-f480-43c1-acf7-7eef4365511b)

Por fim, no UDP o endereço 104.237.170.34 foi o que maior  enviou/recebeu, foram 53.795 pacotes. 

![image](https://github.com/desmonndT/W11-analisando-espionagem/assets/27284652/d1cc7205-7dce-4413-9ecf-25b9f0f1d97e)

