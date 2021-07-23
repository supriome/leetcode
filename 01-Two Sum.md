## 两数相加



```
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
 
var twoSum = function(nums, target) {
    var map = {};
    for (var i = 0; i < nums.length; i++) {
        var compliment = target - nums[i];
        
        if (compliment in map) {
            return [map[compliment], i];
        }
        
        map[nums[i]] = i;
    }
};
```