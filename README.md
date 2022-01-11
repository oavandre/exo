# mage
Projeto open source para pessoas interessadas em Finanças, Investimentos e Análise de Dados


https://www.infomoney.com.br/minhas-financas/confira-o-cnpj-das-acoes-negociadas-em-bolsa-e-saiba-como-declarar-no-imposto-de-renda/




SELECT
	COD_CNPJ,
	cod_pregao.Nome as Nome,
	cod_pregao.Sigla as Sigla,
	RAZAO_SOCIAL,
	NOME_FANTASIA,
	SITUACAO_CADASTRAL,
	DATA_INICIO_ATIVIDADE
 FROM cnpj_capital_aberto CNPJ_DADOS
inner  JOIN cnpj_cod_pregao  cod_pregao ON (cod_pregao.cnpj = CNPJ_DADOS.COD_CNPJ)
ORDER BY RAZAO_SOCIAL
