# Ingestion_into_data_lake

## Azure Storage Explorer
* datalake -> 


## Azure Dev
* Repos
* ENSI-BIG DATA

* ENSI-BIGDATABRICK
```
> KEYRUS
  > data_tranforms
    > raw
      > usr
        > ibge
          > org_raw_deflator_pnad.py
            > cnae
              > org
        > me
          > org_raw_exp_completa.py
> STI_INTELIGENCIA          
  > pipelines..
```
* ENSI-BIGDATADOCS
* ENSI-BIGDATAPRM

## Azure DATA FACTORY
```
> Data Factory
  > "PEN" Icon
    > Create a new branch <Branch name* "uniepro_feature_uld_pintec">
    > Branch < oni_feature_uld_ibge_pintec_cnae #1 >
    > Base on* <master branch>
      > Pipeline    
      
> raw 
  > usr 
    > ibge 
      > org_raw_deflator
       > cnae
        > org_raw_bio_nano_cnae #2
        # databricks: {"notebook":"ibge/pintec/cnae/org_raw_bio_nano_cnae"} #3
        # files: ["{'namespace':'ibge','file_folder':'pintec/cnae/bio_nano_cnae','extension':'csv','column_delimiter':';','encoding':'UTF-8','null_value':''}"] #3
        # env: {"env":"dev"} #3
    > me
      > org_raw_exp_completa
      
> Properties
  > General
    > Name* org_raw_exp_completa

> Parameters
  > databricks {"notebook":"me/org_raw_exp_completa"}
  > files ["{'namespace':'me','file_folder':'exp_completa','extension':'csv','column_delimiter':';','encoding':'UTF-8','null_value':''}"]
  > env {"env":"dev"}
        
```
 
## Azure DataBricks
```
> Repos
  > ENSI-BIGDATABRICKS
    > Pull the branch created early #4
    # Branch < oni_feature_uld_ibge_pintec_cnae > #4
      > KEYRUS
        > raw
          > usr
            > ibge
              > THE FILE WONT BE THERE, THE SO JUST TO CREATE THE FILE org_raw_deflator_pnad.py
            > me
              > THE FILE WONT BE THERE, THE SO JUST TO CREATE THE FILE org_raw_exp_completa.py
              
#4
var_file = {
'namespace': '< ibge> ',
'file_folder': '< pintec/cnae/bio_nano_cnae >',
'extension': 'csv',
'column_delimiter': ';',
'encoding': 'UTF-8',
'null_value': ''
}

var_adf = {
"adf_factory_name": "cnibigdatafactory",
"adf_pipeline_name": "< org_raw_bio_nano_cnae >",
"adf_pipeline_run_id": "60ee3485-4a56-4ad1-99ae-666666666",
"adf_trigger_id": "62bee9e9-acbb-49cc-80f2-666666666",
"adf_trigger_name": "62bee9e9-acbb-49cc-80f2-66666666",
"adf_trigger_time": "2020-06-08T01:42:41.5507749Z",
"adf_trigger_type": "PipelineActivity"
}

var_dls = {"folders":{"landing":"/tmp/dev/uld","error":"/tmp/dev/err","staging":"/tmp/dev/stg","log":"/tmp/dev/log","raw":"/tmp/dev/raw","archive":"/tmp/dev/ach"}, "systems":{"raw":"usr"}}
# /tmp/dev/uld
```
