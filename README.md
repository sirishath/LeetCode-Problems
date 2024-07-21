# LeetCode-Problems


Given an array of integers, return indices of the two numbers such that they add up to a specific target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.
Example:

Given nums = [2, 7, 11, 15], target = 9,
Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].



class Solution {
    public int[] twoSum(int[] nums, int target) {
        int[] newArray = new int[2]; 
        int[] copiedArray = nums; 
        int sum = 0; 
        int size = nums.length; 

        for(int i = 0; i < size - 1; i++){

            int indexOfNum = i; 

            for(int j = 0; j < size; j++){
                if( j != indexOfNum){
                     sum = nums[i] +  nums[j];
                    if(sum == target){
                     newArray[0] = i; 
                     newArray[1] =  j;
           }
                }
            }
        }

        return newArray; 

    }
}
