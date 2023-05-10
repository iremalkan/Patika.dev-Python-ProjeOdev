# Integer, string ve list içeren liste verisini düzeleştirip tek bir liste haline getirmek (flatten)
def flatten_input(lst):
    flatten = []
    for e in lst:
        if isinstance(e, list):
            flatten.extend(flatten_input(e))
        else:
            flatten.append(e)
    return flatten

l = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
flattened_list = flatten_input(l)
print(flattened_list)

# Listenin içindeki elemanları liste halinde bulunan elemanların içindeki değerleri tersine çevirmek
def reverse_list(l):
    l.reverse()
    for e in l:
        if isinstance(e,list):
            reverse_list(e)
            
input=[[1, 2], [3, 4], [5, 6, 7]]
reverse_list(input)
print(input)

