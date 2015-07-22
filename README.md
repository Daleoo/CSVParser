# CSVParser
A PHP CSV Parsing library

## Usage

```
$parser = new CsvParser();
$parser->read('myfile.csv')
    ->match(
      [
        'mykey' => 'myval,
        'myotherkey' => 'myotherval',
      ]
    )
    ->not(
      [
        'mythirdkey' => 'mythirdval',
      ]
    )
    ->write('myoutput.csv');
    
```

In that snippet, we read in a file, and then put all of the rows in the CSV that match the two values put into _CsvParser::match()_ and does not contain the value put into _CsvParser::not()_, then writes the matching rows to _myoutput.csv_
