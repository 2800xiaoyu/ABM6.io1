# ABM6.io1
import csv

def read_data():

    # Read input data
    f = open('C:/Users/xiaoyu/programming/data/input/in (2).txt', newline='')
    data = []
    
    n_rows = 0
    n_cols = None
    
    for line in csv.reader(f, quoting=csv.QUOTE_NONNUMERIC):
        row = []
        for value in line:
            row.append(value)
            # Print(value)
        if n_cols is None:
            n_cols = len(row)
        assert(n_cols == len(row))
        data.append(row)
        n_rows += 1
    f.close()
    return data, n_rows, n_cols
