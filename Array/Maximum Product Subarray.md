https://leetcode.com/problems/maximum-product-subarray/description/
//2018 3 13
//js bird

Find the contiguous subarray within an array (containing at least one number) which has the largest product.

For example, given the array [2,3,-2,4],
the contiguous subarray [2,3] has the largest product = 6.




/**
 * @param {number[]} nums
 * @return {number}
 */
var maxProduct = function(nums) {
    var min=nums[0],max=nums[0],result=nums[0];
    
    for(var i=1;i<nums.length;i++){
        var min1=min
        min=Math.min(min*nums[i],max*nums[i],nums[i]);
        
        max=Math.max(min1*nums[i],max*nums[i],nums[i])
        result=Math.max(result,max)
    }
    return result
};


//����100%����������˼���ǣ�����Զ������Сֵ�����ֵ������Ϊ��Сֵ���������ͻ������ֵ�������ֵ��ɸ����ͻ�����Сֵ�������ϻ���100% ��ͼ��������beats100%����ˬ��


