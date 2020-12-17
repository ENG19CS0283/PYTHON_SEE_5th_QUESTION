# PYTHON_SEE_5th_QUESTION
Program is given in debug_exam.py and Instructions are given in ReadMe file.
# Fork the repository and commit the changes.
# Answers should be given for all three questions here.
5a]
data1 = {1: 4, 3: 3, 4: 4}
data2 = [[1, 2], [2, 2], [3, 3], [4, 9]]
The bug in the program is it is not appending the key value pair which is not present in data1.
5b]
def uniqueUpdate(data1, data2):
    # Initially empty dictionary
    dupKeys = {}
    # Examine every (k, v2) pair in data2
    for [k, v2] in data2:
        # Check if there is a key-value
        # pair with key = k in data1
      
        if k in data1:
        
            v1 = data1[k]
            # (k, v1) in dict1
            # Check if v1 != v2
            if v1 != v2:
                # Add (k, [v1, v2])
                # to dictionary
                dupKeys[k] = [v1, v2]
                # Remove (k, v1) from data1
                del data1[k]
            else:
                # Add (k, v2) to data1
                data1[k] = v2
                # After processing all (k, v2) in
                # data2, return the dictionary
        else:
            data1[k] = v2
    return dupKeys
    
 5c]
 data1 = {1: 4, 3: 3, 4: 4}
 data2 = [[1, 2], [2, 2], [3, 2], [4, 9]]
 output:
    {2: 2}
    [[1, 2], [2, 2], [3, 2], [4, 9]]
    {1: [4, 2], 3: [3, 2], 4: [4, 9]}
    
data1 = {1: 4, 3: 3, 4: 4, 5:1}
data2 = [[1, 2], [2, 2], [3, 2], [4, 9]]
output:
    {5: 1, 2: 2}
    [[1, 2], [2, 2], [3, 2], [4, 9]]
    {1: [4, 2], 3: [3, 2], 4: [4, 9]}
    
