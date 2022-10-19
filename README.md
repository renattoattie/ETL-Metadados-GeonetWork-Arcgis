ETL usando Pentaho Data Integration - PDI para captura de Metadados do ARCGIS
Enterprise.

Essa rotina foi utlizada para capturar dados públicos da api REST ARCGIS
do SISDIA 

Esse sistema está sobre a administração da SEMA-DF.

No entanto, pode ser utilizado para qualquer API REST do ARCGIS.

Ações de Customização:

1. Deve-se setar e criar a pasta que vai receber os metadados na
transformação: trf_downloads_METADADOS

2. Deve-se setar os parâmetros da URL na transformação: trf_downloads_METADADOS

3. Deve-se criar um banco no Postgres e setar sua conexão nas transformações:
trf_atualiza_links_WMS_WFS_1
trf_atualiza_links_WMS_WFS_2
trf_atualiza_links_ARCGIS
trf_atualiza_THUMBNAIL


Ações de integração com o Geonetwork:

1. Execute a transformação: trf_downloads_METADADOS
2. Abra o Geonetwork e vá na opção adicionar dados e sete a pasta onde foi efetuado o downalod dos metadados pelo Pentaho.
3. Execute as outras transformações para atualizar links e thumbnails na ordem:
3.1 trf_atualiza_links_WMS_WFS_1
3.2 trf_atualiza_links_WMS_WFS_2
3.3 trf_atualiza_links_ARCGIS
3.4 trf_atualiza_THUMBNAIL
