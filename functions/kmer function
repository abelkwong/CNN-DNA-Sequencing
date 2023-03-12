string_1 = "GATTACA"
string_2 = "MISSISSIPPI"
ksize_1 = 4
ksize_2 = 5

def get_Kmer(string, k):
    for i in range(len(string) - k + 1):
        print(string[i:i+k])

def get_prefixes_and_suffixes(string, k):
    for i in range(len(string) - k + 1):
        print(string[i:i+k-1] + " " + string[i+1:i+k])

get_Kmer(string_1, ksize_1)
print("----------------")
get_Kmer(string_2, ksize_2)
print("c")
get_prefixes_and_suffixes(string_1, ksize_1)
print("----------------")
get_prefixes_and_suffixes(string_2, ksize_2)