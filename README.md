# product_ofArray_except_self
python code for product of array except self 

def product_except_self(nums):
    pre_pro=[1]*len(nums)
    post_pro=[1]*len(nums)
    res=[0]*len(nums)
    for i  in range(1,len(nums)):
        pre_pro[i]=nums[i-1]*pre_pro[i-1]
    for i in range(len(nums)- 2, -1, -1):
        post_pro[i]=nums[i+1]*post_pro[i+1]
    for i in range(len(nums)):
        res[i]=pre_pro[i]*post_pro[i]
    return res
print(product_except_self([1,2,3,4,5]))

        
        
        
        
        
    
        
        
        
    

