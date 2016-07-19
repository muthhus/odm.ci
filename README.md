# odm.ci
Baseado no artigo http://www-01.ibm.com/support/docview.wss?uid=swg21663707

# Exemplos de uso

To generate the security report: 
ant -f dcBuild.xml  security-report 

To deploy a ruleapp: 

``ant -f dcBuild.xml  deploy-ruleapp -DresUrl=http://localhost:9080/res -DresUser=resAdmin -DresPassword=resAdmin -Druleapp=MyRuleApp``

To deploy a ruleapp and create a baseline: 

``ant -f dcBuild.xml  deploy-ruleapp -DresUrl=http://localhost:9080/res -DresUser=resAdmin -DresPassword=resAdmin -Druleapp=MyRuleApp -Dbaseline="June Release"`` 

To deploy a ruleapp and increment the minor ruleapp version:

``ant -f dcBuild.xml  deploy-ruleapp -DresUrl=http://localhost:9080/res -DresUser=resAdmin -DresPassword=resAdmin -Druleapp=MyRuleApp -Dpolicy=MINOR_RULEAPP`` 

To redeploy a ruleapp : 

``ant -f dcBuild.xml  redeploy-ruleapp -DresUrl=http://localhost:9080/res -DresUser=resAdmin -DresPassword=resAdmin -Druleapp=MyRuleApp -Dbaseline="June Release"`` 

To extract a ruleapp archive : 

``ant -f dcBuild.xml  extract-ruleapp -Druleapp=MyRuleApp``

To extract a ruleapp archive and create a baseline: 

``ant -f dcBuild.xml  extract-ruleapp -Druleapp=MyRuleApp -Dbaseline="June Release"``

To extract a ruleapp archive from an existing baseline: 

``ant -f dcBuild.xml  extract-ruleapp -Druleapp=MyRuleApp -DfromBaseline="June Release"``
