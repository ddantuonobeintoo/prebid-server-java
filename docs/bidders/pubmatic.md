# PubMatic Bidder

## Test Request

The following test parameters can be used to verify that Prebid Server is working properly with the 
PubMatic adapter. This example includes an `imp` object with an PubMatic test publisher ID, ad slot,
and sizes that would match with the test creative.

```
"imp":[
      {
         "id":â"some-impression-idâ,
         "banner":{
            "format":[
               {
                  "w":300,
                  "h":250
               },
               {
                  "w":300,
                  "h":600
               }
            ]
         },
         "ext":{
            "prebid": {
               "bidder"{
                  "pubmatic":{
                     "publisherId":â156276â,
                     "adSlot":"pubmatic_test"
                  }
               }
            }
         }
      }
   ]
```