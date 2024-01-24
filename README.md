# Production Ready Development Practice

* org
  * orgid : 2848a844-05a7-4de3-ab5d-b40cdb24fc20
  * client id : 85317fa0b55c42e3babaa7584ff2b0bb
  * client secret : 25CbA0d940d24b4cb8FC498c3DC48196

* connectedapps
  * exchange viewer
    * client id : e3c39ea8dc504e7da7f23604f74917ac
    * client secret : 865F3Ae0C38247a7a692457713a650dF
  * exchange contributor
    * client id : d9c5f574f483416e8fee4b136a6bea89
    * client secret : c477E679ff7C4FDC86FE94D2ad441930
  * cloudhub deployment
    * client id : 8f7a655357d947a29ffc2c24a8c09cc7
    * client secret : a3d95d84F4824A45b18cBaddE2C56009
* apikey
  * prod : 19250261
  * stg : 
  * dev : 

-M-Danypoint.platform.client_id=85317fa0b55c42e3babaa7584ff2b0bb
-M-Danypoint.platform.client_secret=25CbA0d940d24b4cb8FC498c3DC48196


mvn -DmuleDeploy deploy -Dap.client_id=85317fa0b55c42e3babaa7584ff2b0bb -Dap.client_secret=25CbA0d940d24b4cb8FC498c3DC48196 -Dap.ca.client_id=8f7a655357d947a29ffc2c24a8c09cc7 -Dap.ca.client_secret=a3d95d84F4824A45b18cBaddE2C56009

//
mvn -DmuleDeploy deploy -Dap.client_id=85317fa0b55c42e3babaa7584ff2b0bb -Dap.client_secret=25CbA0d940d24b4cb8FC498c3DC48196 -Dap.ca.client_id=8f7a655357d947a29ffc2c24a8c09cc7 -Dap.ca.client_secret=a3d95d84F4824A45b18cBaddE2C56009 -Dencrypt.key=secure12345 -Ddeployment.env=dev -DskipTests=true

mvn -DmuleDeploy deploy -Dap.client_id=85317fa0b55c42e3babaa7584ff2b0bb -Dap.client_secret=25CbA0d940d24b4cb8FC498c3DC48196 -Dap.ca.client_id=8f7a655357d947a29ffc2c24a8c09cc7 -Dap.ca.client_secret=a3d95d84F4824A45b18cBaddE2C56009 -Dencrypt.key=secure12345 -Ddeployment.env=stg -DskipTests=true

mvn -DmuleDeploy deploy -Dap.client_id=85317fa0b55c42e3babaa7584ff2b0bb -Dap.client_secret=25CbA0d940d24b4cb8FC498c3DC48196 -Dap.ca.client_id=8f7a655357d947a29ffc2c24a8c09cc7 -Dap.ca.client_secret=a3d95d84F4824A45b18cBaddE2C56009 -Dencrypt.key=secure12345 -Ddeployment.env=prod -Ddeployment.suffix= -DskipTests=true