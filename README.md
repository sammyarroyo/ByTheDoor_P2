# ByTheDoor_P2
Project #2 for the group By The Door


# Project 2

#!/usr/bin/env python3
import io, re
import argparse
import numpy

#Open a new blank file to save info to later, make this new file a variable called "new_file"
with open('new_CF4_averages.tsv', 'w') as new_file:

#Use arg parse to set the file for reading as a variable named "working_file".
#This code block will allow us to use the name of the file used to run the script
#from the command line
        parser = argparse.ArgumentParser(
                description="Average FPKM values for 4 CF4 biological replicates.")
        parser.add_argument('filename')
        args = parser.parse_args()
        working_file = open(args.filename)
