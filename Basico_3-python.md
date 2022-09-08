### Display Colors
Write a Python program to display the first and last colors from the following list color_list = ["Red","Green","White" ,"Black"]

https://www.geeksforgeeks.org/print-colors-python-terminal/

https://en.wikipedia.org/wiki/ANSI_escape_code#Colors

https://stackoverflow.com/questions/287871/how-do-i-print-colored-text-to-the-terminal

 how to print colored text in Python using several methods to output colored text to the terminal in Python. 

The most common ways to do this are using:

Using colorama Module

    from colorama import Fore, Back, Style
    print(Fore.RED + 'some red text')
    print(Back.GREEN + 'and with a green background')
    print(Style.DIM + 'and in dim text')
    print(Style.RESET_ALL)
    print('back to normal now')


Using termcolor Module
Using ANSI Code in Python
The most common way to print colored text is by printing ANSI escape sequences directly. This can be delivered in different formats such as: 

Example 1: Build Functions to call . 
We can build functions to call particular color named functions to execute the relevant ANSI Escape Sequence. The below is Python program to print colored text and background

Example 2: Build a class of colors: 
Create a class to allot background and foreground colors and call them. The below is Python program to print colored text and background.


    class colors:


    '''Colors class:reset all colors with colors.reset; two
    sub classes fg for foreground
    and bg for background; use as colors.subclass.colorname.
    i.e. colors.fg.red or colors.bg.greenalso, the generic bold, disable,
    underline, reverse, strike through,
    and invisible work with the main class i.e. colors.bold'''
    reset = '\033[0m'
    bold = '\033[01m'
    disable = '\033[02m'
    underline = '\033[04m'
    reverse = '\033[07m'
     strikethrough = '\033[09m'
      invisible = '\033[08m'

       class fg:
            black = '\033[30m'
            red = '\033[31m'
            green = '\033[32m'
            orange = '\033[33m'
            blue = '\033[34m'
            purple = '\033[35m'
            cyan = '\033[36m'
            lightgrey = '\033[37m'
            darkgrey = '\033[90m'
            lightred = '\033[91m'
            lightgreen = '\033[92m'
            yellow = '\033[93m'
            lightblue = '\033[94m'
            pink = '\033[95m'
            lightcyan = '\033[96m'

        class bg:
            black = '\033[40m'
            red = '\033[41m'
            green = '\033[42m'
            orange = '\033[43m'
            blue = '\033[44m'
            purple = '\033[45m'
            cyan = '\033[46m'
            lightgrey = '\033[47m'

    print(colors.bg.green, "SKk", colors.fg.red, "Amartya")
    print(colors.bg.lightgrey, "SKk", colors.fg.red, "Amartya")
    
    
Example 3: Iterating functions

We can design iterating & self-generating ANSI Escape sequence, functions. The below is Python program to print colored text and background

    def print_format_table():
        """
        prints table of formatted text format options
        """
        for style in range(8):
            for fg in range(30, 38):
                s1 = ''
                for bg in range(40, 48):
                    format = ';'.join([str(style), str(fg), str(bg)])
                    s1 += '\x1b[%sm %s \x1b[0m' % (format, format)
                print(s1)
            print('\n')


    print_format_table()


otra forma es:

    class bcolors:
        HEADER = '\033[95m'
        OKBLUE = '\033[94m'
        OKCYAN = '\033[96m'
        OKGREEN = '\033[92m'
        WARNING = '\033[93m'
        FAIL = '\033[91m'
        ENDC = '\033[0m'
        BOLD = '\033[1m'
        UNDERLINE = '\033[4m'
    #forma 1
    print(bcolors.UNDERLINE + "Warning: No active frommets remain. Continue?" + bcolors.ENDC)
    #forma 2 
    print(f"{bcolors.WARNING}Warning: No active frommets remain. Continue?{bcolors.ENDC}")

"curses" module, which handles a lot of the complicated parts of this for you. The Python Curses HowTO is a good introduction.
If you are not using extended ASCII (i.e., not on a PC), you are stuck with the ASCII characters below 127, and '#' or '@' is probably your best bet for a block.

https://www.mclibre.org/consultar/python/ejercicios/ej-ascii-1.html

    alto = int(input("Alto"))
    ancho = int(input("Ancho"))
    num_h= int(input("h"))
    num_v= int(input("v"))

    for i in range (0,num_v):
      print ("*  "*ancho*num_h)
      for i in range (0,alto-2):
       print('*','   '*(ancho-2)*num_h),('*')
    print ("*  "*ancho*num_h)

¿Cómo hacer que se mantengan los números en la pantalla? como en una calculadora sin tener que hacer mucho proceso
Elabora los siguientes pseudocódigos:

