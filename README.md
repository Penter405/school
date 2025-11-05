# 資料科學

<img width="713" height="305" alt="image" src="https://github.com/user-attachments/assets/9b21317d-5a47-458c-9d6f-01099334cd4c" />

<img width="1609" height="363" alt="image" src="https://github.com/user-attachments/assets/608f460f-d7d6-4363-96e4-efa7b6654f05" />

<img width="1562" height="358" alt="image" src="https://github.com/user-attachments/assets/f5395139-c004-4877-a933-354500aa702c" />

<img width="1794" height="341" alt="image" src="https://github.com/user-attachments/assets/f94842e2-1c16-480d-b20f-147ea88c81ee" />

<img width="335" height="97" alt="image" src="https://github.com/user-attachments/assets/0ce063b0-6f02-4cce-8804-910d691e23c1" />

<img width="1285" height="315" alt="image" src="https://github.com/user-attachments/assets/2c14a427-9421-4669-93f6-e7ba0d4599bf" />


class tree():
    def __init__(self,val):
        self.val=val
        self.right="-"
        self.left="-"


def set():
    """set tree"""
    time=-1
    hash={}
    for rs in input().split(")"):
        
        time+=1
        ob=rs[1:].split(',')
        for pe in ob:
            
            if pe != "-" and pe not in hash:
                hash[pe]=tree(int(pe))
            
                
        node=hash[ob[0]]
        if time==0:
            root=node
        if ob[1]!="-":
            node.left=hash[ob[1]]
        if ob[2]!="-":
            node.right=hash[ob[2]]

    '''print("\n\n\n")
    print(root.val)
    print(root.right)
    print(root.left)
    print(root.left.val)
    print(root.right.val)
    '''
    return root
root=set()
"""print("\n\n\n")
print(root.val)
print(root.right)
print(root.left)
print(root.left.val)
print(root.right.val)
exit()
"""
"""
print(root.val)
print(root.left)
print(root.right)
"""
#int is immoutable

"""
function always think -
"""

def dfs_postorder():
    result=[]
    def fun(root,deep):
        result.append(root.val)#before stop, do result
        if root.left=="-" and root.right=="-":
            return deep
            #if 眼前是垃圾  ,then stop 

        if root.left !="-":
            le=fun(root.left,deep+1)

        if root.right !="-":
            ri=fun(root.right,deep+1)




    fun(root,0)
    return ",".join(result)



print(dfs_postorder())
