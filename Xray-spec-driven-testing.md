https://docs.getxray.app/space/XRAYCLOUD/44565229/Using+Generic+Tests+for+Automation  
https://docs.getxray.app/space/XRAY/301667997/Import+Execution+Results+-+REST#xUnit%C2%A0XML-results  

────────────────────────────────────────────────  
          1. Create spec in Jira                
  Acceptance criteria added to Jira story     
────────────────────────────────────────────────  
                     ⬇️  
────────────────────────────────────────────────  
     2. Create generic test in Jira Xray        
 Jira Xray generic test has unique name       
────────────────────────────────────────────────  
                     ⬇️  
────────────────────────────────────────────────  
     3. Implement C# test with unique name      
      Developer/AI writes xUnit test          
────────────────────────────────────────────────  
                     ⬇️  
────────────────────────────────────────────────  
        4. GitHub pipeline execution            
     Pipeline triggers "dotnet test"          
────────────────────────────────────────────────  
                     ⬇️  
────────────────────────────────────────────────  
        5. Get xUnit XML test results           
   Pipeline gets "test-results.xml"           
────────────────────────────────────────────────  
                     ⬇️  
────────────────────────────────────────────────  
  6. Import test results to Jira Xray via API   
 Results update Jira story and test           
────────────────────────────────────────────────  
  
