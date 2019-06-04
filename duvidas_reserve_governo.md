# SelfBooking

Endpoint: https://wsct.casablancaturismo.com.br/selfbooking

## Campos para avaliar com reserve
Objeto Reserva
 1. list_historico
 2. tipo_passageiro
 3. cargo_passageiro
 4. solicitante: Os dados do solicitante não vem com cpf
 5. consultor.horarios: Dados não recebidos no xml
 6. Endereços/Localizações com informações incompletas
 7. Origem: Nenhuma informaçõa vinda no xml 
 8. Fornecedor: Não informado no xml
 9. list_remarcacoes: O Xml não fornece a lista remarcações 
 10. 

## Campos para avaliar com Governo
Objeto Reserva
 1. taxa: Receber os campos iguais ao do reserve ou relizar um "de/para"?
 2. data_inicio/data_fim: Para data inicio pegar o "menor" dia da reserva e para data fim "maior" dia da reserva independente do produto?
 3. qtde_diarias: calcular dias do inicio da reserva e fim da reserva?
 

## Objetos de Endereço/Destino/LocaEntrega
Vindo do reserve alguns campos recebem apenas nos seguintes formatos:
 - Nome da cidade
 - Nome da cidade/IATA
 - IATA
 - Nulo/Vazio
Até o reserve modificar os dados e enviar corretamente os dados foi criado um campo nomeado de "observacoes" com toda e qualquer informação vinda do xml.

## Agendamentos
Para novos pedidos: ciclo de 10 minutos
Atualizações de dados do pedido: Ciclo de 24 horas iniciado durante as 00:00 
Atualização de dados de consultor, passageiro, solicitante: Ciclo de 24 horas iniciando durante as 03:00

## Parâmetros de filtro
TIPO_DATA: 
 - DATA_EMISSAO
 - DATA_AUTORIZACAO
 - DATA_CRIACAO
 
 ~~DATA_INICIO~~ * *Ao ter informações corrigidas o filtro irá funcionar*
 ~~DATA_FIM~~ * *Ao ter informações corrigidas o filtro irá funcionar*

## Parâmetros de filtro adicionais
TIPO_SERVICO
 - 1 - Aéreo
 - 2 - Hotel
 - 3 - Carro
 - 4 - Seguro
 - 5 - Rodoviário
 
 

> Todos os parâmetros de filtro são recebidos através de método GET

 

