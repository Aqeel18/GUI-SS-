Two Pass Assembler Code Analysis
Overview
The provided code implements a Two Pass Assembler in a web-based interface using HTML, CSS, and JavaScript. The assembler processes assembly language code, converting it into machine code through two distinct passes: Pass 1 for symbol resolution and Pass 2 for object code generation. Users can input assembly code manually or upload it from a file, and they can similarly provide an opcode table (OPTAB).

Structure
HTML
Head Section:

Includes meta tags for character set and viewport settings.
Sets the title of the document.
Contains a <style> block for CSS styles.
Body Section:

Contains a main <div> with the class "container" that houses all user interface elements.
Organized into sections for inputting OPTAB, assembly code, buttons for processing, and output areas.
CSS
Defines styles for the body, container, headings, labels, text areas, buttons, and various other elements.
The design aims for a modern look with contrasting colors for readability and user experience.
JavaScript
Global Variables:

Manages state and holds content for input files, symbol tables (SYMTAB), location counters, and outputs.

Functionality:

File Upload Handling:

Reads assembly code and OPTAB from text files using the FileReader API.
Populates respective text areas with file content.
OPTAB Parsing:

Converts the content of the OPTAB text area into a JavaScript object for easy access to opcodes by mnemonics.
Pass 1 Logic:

Parses assembly code line by line to:
Identify START and END directives.
Update the location counter (locctr).
Build a symbol table (symtab) for labels.
Generate output for the intermediate file and program length.
Outputs results to designated text areas.
Pass 2 Logic:

Generates the assembly listing and object program by:
Translating mnemonics into object codes using the parsed OPTAB and SYMTAB.
Creating header and end records for the object program.
Building text records as necessary.
Outputs the assembly listing and object program to the corresponding text areas.

Inputs:

Users can upload input assembly code and OPTAB text files.

Outputs:

Intermediate results are displayed in read-only text areas, providing clear feedback on the assembler's processing.
Functionality Summary

Pass Execution:

The first pass analyzes the assembly code to determine symbol addresses and calculate program length.
The second pass translates assembly instructions into machine code, generating object code and assembly listings.
Output Generation:

Outputs are formatted for readability, showing the results of both passes and the final object program.
Conclusion
This Two Pass Assembler provides an interactive web-based environment for users to assemble simple assembly code into object code. It supports file uploads for both assembly code and the OPTAB, processes the input through two distinct passes, and displays comprehensive output, including an intermediate file, symbol table, program length, assembly listing, and object program. The structure is user-friendly, allowing for efficient operation and clear feedback on the assembler's processes.
