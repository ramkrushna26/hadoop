```
scan '<TABLE>', {LIMIT=>2}  

scan '<TABLE>', {FILTER=>"RowFilter(=,'binary:<VALUE>')"}   

scan '<TABLE>', {FILTER=>"RowFilter(=,'binaryprefix:<VALUE>')"}  
  
scan '<TABLE>', {FILTER=>"ValueFilter(=,'binaryprefix:<VALUE>')"}  

scan '<TABLE>', {FILTER=>"ValueFilter(=,'substring:<VALUE>')"}

scan 'tableName', {FILTER=>"SingleColumnValueFilter ('column family','col1',=,'regexstring:.*hey.*')"}
```
