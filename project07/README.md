# Introduction
Description of the project

# Pseudocode
Put pseudocode in this box:

```
1. BWT function:
- create an empty list
- loop through each index of the input string
    - create a rotation by: taking substirng from index i to end, then add substring from start to index i
    - add generated rotation to the list
- sort list in alphabetical order
- create an empty string for BWT result
- loop through each sorted rotation 
    - append the last character of the rotation to the BWI string
- return the BWI string

2. suffix_array
- create an empty list to store suffixes
- loop through the string by index 
    - create suffix starting from index i
    - append suffix and i as tuple to the suffixest list
- sort suffixes list
- create empty indexes list
- loop through sorted suffixes list
    - append each index to the indexes list
- return indexes list

3. BWT_from_suffix_array
- create an empty BWI string
- loop through each position in suffix list
    - if position = 0, then add last character of text to BWI string.
    - otherwise, add text[position -1] to BWI string
- return BWI string

4. cal_count
# Step 1: Count frequency of each character
    char_counts ← count occurrences of each character in string
# Step 2: Sort characters lexicographically
    sorted_chars ← sorted list of unique characters in string
# Step 3: Initialize output dictionary and cumulative counter
    smaller_counts ← empty dictionary
    cumulative ← 0
# Step 4: Compute number of smaller characters
    FOR each char IN sorted_chars:
        smaller_counts[char] ← cumulative
        cumulative ← cumulative + char_counts[char]
# Step 5: Return result    

5. cal_occur
- find and sort unique character from input bwt string
- create an empty occurency dictionary
- loop through each unique character, then create a list of zeroes with the same length as the bwt string
- loop through the bwt string:
    - identify the current character
    - if not the first posistion -> copy from the previou position for all characters
    - increase the count for the current character by one
- return the dictionary for occurence counts

6. update_range
- start with the current range defined by lower and upper
- for the given character a, compute the new lower boundary"
    - if lower boundary is 0:
        - set new lower to the starting position of the character a.
    - else: add the number of occurences of a before the lower boundary to the starting position of a. 
- compute the new upper bound:
    - add the number of occurence of a up to the upper boundary to the starting position of a
    - substract one to get the correct ending index
- return the updated lower and upper boundaries.

7. find_match
- add the end market to the reference string
- build the suffix array of the reference
- build the bwt string from the suffix array
- find count characters lexicographically smaller than each character
- find occurrences of each character up to each position
- set lower and upper as full range of reference
- read query from right to left
    - for each character, update the range using the count and occurence tables.
    - if the range become invalid, return an empty list. 
- after processing the whole query, use the suffix array position in the final range as match positions.
- sort the match positions and return them

8. run_length_encode
- if input string is empty, return an empty result
- set current character to the first character of the string
- set counter to 1
- create an empty string to store the encoded result
- scan through the string starting with second character to the end
- for each character:
    - if it's the same with the current chacteract -> increase counter by 1
    - otherwise:
        - add the current character and its count to the result
        - update current character to this new character
        - reset the counter to 1
- return encoded string

9. 
```

# Successes
Description of the team's learning points

# Struggles
Description of the stumbling blocks the team experienced

# Personal Reflections
## Group Leader
Group leader's reflection on the project

## Other member
Other members' reflections on the project

# Generative AI Appendix
As per the syllabus
