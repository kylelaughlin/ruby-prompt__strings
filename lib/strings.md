---
title: Strings
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is a String?

A string is a series of characters treated as one unit. A string can include letters, digits, spaces, special characters, 
and punctuation and are typically enclosed in double or single quotes depending on the syntax of the language being used.

# What are some examples of information that would be Strings as opposed to some other data type?

While you would use an integer to store whole numbers, like a person's age, you would use a sting hold the peron's name, their 
drivers licenses number (combination of letters and numbers), their pet's name, and the name of their favorite restaurant.

# What is one way, using Ruby, to retrieve the 6th character in a String like `"Ada Lovelace"`? How about the 8th character? What happens if you try to retrieve the value of the _99th_ character (Or any character that doesn't exist)?

One way to retrieve the 6th character in "Ada Lovelace" (which is the character 'o') is to write "Ada Lovelace"[6-1].
Two things 1) 6 represents the nth character you want. 2) 1 must be subtracted from 6 becuase strings, like arrays, are 
zero based so the index of the first character is actually 0. You can also save the string to a variable and write something 
like this: my_string[n-1] to get the nth character of the sting. If we wanted to get the eighth charater in "Ada Lovelace", the
'e', we would substitute an 8 for the 6 above. If we tried to retrieve the 99th character we would be returned nil becuase the 99th character is nothing since it does not exist 
in the string. 

# The previous question asks about finding, for example, the 6th character in a String. Is it possible to find the **-6th** (Notice the negative symbol!) character in a String? What does that even mean?

To find the -6th character of the string means to find the 6th character from the end of the string. The example 
"Ada Lovelace"[-6] would return 'v'. We do not need to subtract as we do not have to deal with the zero at the begining since we 
are moving right to left.

# What is one way, using Ruby, to replace certain characters in a string with some other set of characters? For example, given `"Sumeet Jain"`, how would you replace all of the `e` characters in my name with exclamation marks? (So it would be `"Sum!!t Jain"`.)

A way to replace a certain character, or pattern of characters, is to use the gsub method on the string. This method looks
for a character or pattern of characters and replaces them with another character or pattern of characters. To replace the 
'e's in "Sumeet Jain" with '!'s we would write "Sumeet Jain".gsub("e","!"). We would save our original string to a variable 
and run the gsub method on that variable. If our variable was called name we would write name.gsub("e","!").  If we wanted 
the gsub method to alter the original string stored in a variable we could write name.gsub!("e","!"). So the next time we 
called upon the variable name all of the 'e's would still be '!'s.