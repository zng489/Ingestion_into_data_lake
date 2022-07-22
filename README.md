# Ingestion_into_data_lake

```
## git clone ENSI-BIGDATACRAWLER (repos)
  -> Developement bot
    -> git init
    -> git username
    -> git password
    -> git checkout -b org_raw_rfb_cno
    -> git add --all
    -> git commit -m "message"
    -> git push -u origin org_raww_rfb_cno
      -> Pull Request para branch "dev"


-------------------------------------------------------------------------------------------

## DATA FACTORY:
* (folder) "crw"
  -> (folder) "rfb_cno"
    -> (pipelines) "lnd_org_raw_rfb_cno"
        parameter
        
        name Type     Default
        bot  String   org_raw_rfb_cno
        env  Object   {"env":"dev"}
          -> Pull Request para master
          
 ## The merge problem that I've met:
  -> For instance:
    -> org_raw_rfb_cno -> dev: Conflict problem, so to resolve this problem
      -> First: Create a new branch based on "dev"
      -> Second: Commit the new branch with "dev"
  

## Factory Resources:
  => workflow
    => workflow_prod_lnd
      => Parameters
      Name  |  Type    |   Default value
      env   |  Object  |   {"env":"dev"}
      bot   |  String  |  org_raw_rfb_cno
      
    => Execute Pipeline
      => Name*: lnd_org_raw_rfb_cno
      
        => Settings
        Invoked pipeline: lnd_org_raw_rfb_cno
        
      Name  |  Type    |    Value                      |    Default value
      env   |  Object  |    @pipeline().parameters.env |    {"env":"dev"}
      bot   |  String  |    Value                      |    org_raw_rfb_cno
 
-------------------------------------------------------------------------------------------
## WorkFlow Logic:
=> lnd_org_raw_rfb_cno =====> wkf_lnd_uniepro_movie_4_hours =====> 


-------------------------------------------------------------------------------------------
## Ingestion of PRM:
=> Azure DevOps
  => ENSI-BIGDATAPRM
    => prm
      => usr
        => Creating new branch "org_raw_rfb_cno"
        => Creating new folder "rfb_cno"
        => Adding the excel file "PRM"
        => Pull request
  
  
## Pay attention:
=> Manage -> Triggers -> Cancel trigger
``` 










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
  
# 6  
# Repos
> New pull request
> < oni_feature_uld_ibge_pintec_cnae >

> Pipelie
  
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

var_dls = {"folders":{"landing":"/tmp/dev/uld","error":"/tmp/dev/err","staging":"/tmp/dev/stg","log":"/tmp/dev/log","raw":"/tmp/dev/raw","archive":"/tmp/dev/ach"}, "systems":{"raw":"/tmp/dev/usr"}}
# /tmp/dev/uld

#5

> 

> Commit & Push!!!
```
