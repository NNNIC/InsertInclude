# InsertInclude
Include a text file at the point that is indicated to include the file.  I created this tool for the C# using section to stop changing many times.

# How to use

1. Create a text file for include.

ex) using_text.txt

    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    using System.IO;
    using System.Text.RegularExpressions;

2. Write include mark in source.

Format:  
    //<<<include=FILENAME     --- begin mark with FILENAME
    //>>>                     --- end   mark


ex) hoge.cs
    //<<<include=using_text.txt
    using System;
    using System.Collections.Generic;
    //>>>


3. Execute the tool

The tool traverse all cs files from the specified folder and subsutitute the text by reading the specified file between the beging mark and the end mark.
The specified file is searching  in the specified folder.

InsertInlucde  {folder that has the insert text} {folder to start traversing}





