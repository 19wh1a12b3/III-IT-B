
int removeElement(int* nums, int numsSize, int val){  
    int act_pos = 0;
    int temp = 0;
    for(int i=0;i<numsSize; i++){
        if(nums[i] != val){
            temp=nums[i];
            nums[i]=val;
            nums[act_pos]=temp;
            act_pos++;
        }                 
    }
return act_pos;
}
