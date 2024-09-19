# Desafio de Projeto: Coleta e Processamento de Dados com o Power Query

ℹ️ **Nota:** Este projeto foi desenvolvido durante o curso “Processamento de Dados com o Power BI” ministrado por [Juliana Mascarenhas](https://www.linkedin.com/in/juliana-mascarenhas-ds/) na [DIO](https://web.dio.me).

Neste projeto, foi criada uma instância no Azure para o MySQL, e o banco de dados `azure_company` foi configurado. A integração com o Power BI e o MySQL no Azure foi realizada com sucesso. Durante o processo de transformação de dados no Power Query, os seguintes passos foram seguidos:

1. Os cabeçalhos e os tipos de dados foram verificados;
2. Os valores dos salários foram convertidos para o tipo decimal fixo;
3. Um valor nulo foi identificado na coluna `super_ssn`, que não pôde ser removido, pois indica o gerente geral, James Borg;
4. O gerente geral possui um campo nulo no `super_ssn`;
5. Todos os departamentos têm gerentes, porém as datas de início e término das gerências apresentam inconsistências (a data de início é posterior à data de término);
6. Não foi identificado nenhum departamento sem gerente;
7. As horas dedicadas aos projetos foram verificadas e parecem estar dentro do esperado;
8. A coluna de endereço foi separada em: número, logradouro, cidade e estado;
9. As tabelas `employee` e `department` foram mescladas (inner join), garantindo que apenas linhas correspondentes fossem unidas, já que todos os funcionários têm um departamento associado;
10. Colunas desnecessárias foram eliminadas de todas as tabelas, inclusive nas mesclas;
11. A mescla dos colaboradores com seus respectivos gerentes foi realizada no Power Query;
12. As colunas de nome, segundo nome e sobrenome dos colaboradores foram mescladas em uma única coluna de nome completo;
13. Os nomes dos departamentos foram mesclados com suas localizações (right join) para garantir que todos os locais fossem associados a um departamento;
14. A mescla foi utilizada em vez de atribuir, devido à relação de vários para vários entre locais e departamentos, onde é necessário preservar a integridade referencial entre essas tabelas;
15. Os dados foram agrupados por gerente na nova tabela "manager employee", e a contagem do número de colaboradores supervisionados por cada gerente foi realizada;
16. Colunas irrelevantes para o relatório final foram removidas.

Por fim, foi gerado um relatório no Power BI com os dados devidamente limpos e transformados:



![Print do Relatório](https://github.com/orlandoabreugomes/desafio-azure-company/blob/main/outcome/relatorio_azure_company.png)



📒[Relatório no formato PDF](https://github.com/orlandoabreugomes/desafio-azure-company/blob/main/outcome/desafio_azure_company.pdf)

## 🖥️ Tecnologias utilizadas no Projeto:

* [Power BI](https://www.microsoft.com/pt-br/power-platform/products/power-bi)


## 🙍🏽 Profissional
Orlando Gomes
[GitHub](https://github.com/orlandoabreugomes) | [Linkedin](https://www.linkedin.com/in/orlandoabreugomes/) | [e-mail](mailto:gomes.oa@gmail.com)
