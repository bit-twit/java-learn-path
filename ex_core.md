# Exercises - Core

## 1.1 Words and lines

Write a console program that reads an input *.txt file and outputs the number of lines and words in that file.

### Details

* The file name should be read from console as a parameter.
* Define a FileStructure Java class that retains all the necessary file information: filename, nr lines, nr words.
* Build a function that receives a String and returns number of words in that String.
* Build a function that receives a File as parameter and returns a complete FileStructure.
* Print the FileStructure to the console.

### Example

    $ java WordsAndLines.clas test.txt
    ;;=> [filename: 'test.txt', nrLines: '200', nrWords:'1200']

### Further reading

* Reading lines from text files in Java - http://www.mkyong.com/java/how-to-read-file-from-java-bufferedreader-example/

## 1.2 Bubblesort

Build a console program that reads an input file with numbers and writes an output file with the numbers sorted using the bubblesort algorithm.

### Details

* Build a function that receives a File and return a List of numbers read from that File.
* Build a function that receives a List of numbers and returns another List with the numbers sorted.
* Build a function that takes a List of numbers and a File, and writes the given List to the File.
* Package your application as JAR.

### Example

    ;; input file format
    nr_numbers
    nr1 nr2 nr3 ...

    ;; output file format
    nr_numbers
    nr1 nr2 nr3 ...

    $ java -jar bubblesort.jar input.txt
    ;; => Results written to output.txt

### Further reading

* Bubblesort algorithm - http://www.sorting-algorithms.com/bubble-sort

## 1.3 Currency converter

Build a console program that converts between RON, USD, and EUR in realtime (using a third-party service).

### Details

* The program should first show a menu with options:

  + convert from RON -> USD
  + convert from RON -> EUR
  + convert from USD -> RON
  + convert from USD -> EUR
  + convert from EUR -> RON
  + convert from EUR -> USD

* Build a function that keeps showing a menu and waits for the user to input an option
* Build a function that receives/parses the RON,EUR,USD currency values from a third-party service (Ex: parse the HTML page from www.bnr.ro)
* Build a Converter class with overloaded functions for all three currency transformations (Hint: define numeric Classes for each of the currency, wrapping a Long value)
* for each option that the user chooses, compute the conversion and print the result.

## 1.4 CNP validator

Write a console program that receives as parameter a romanian CNP number and validates it.

### Further reading

* CNP format - https://ro.wikipedia.org/wiki/Cod_numeric_personal
* Online validator - http://www.validare.ro/validare-cnp.html

## 1.5 HTML parser

Write a console program that reads a given URL and parses the HTML described by that URL displaying various information about it:
* nr words
* most frequent 10 words
* first 100 words sorted by frequency

### Details

* use the tree implementation from the Huffman coding algorithm

### Further reading

* Huffman algorithm - https://en.wikipedia.org/wiki/Huffman_coding
