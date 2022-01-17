# SeemsEasybutdifficult
Missing number

Find All Numbers Disappeared in an Array:
test:[1,5, 3, 4, 7]
ans: [2, 6]
The solution must be in JAVA

import java.util.Arrays;
import java.util.HashSet;
import java.util.Set;

public class Test {
    public static <T> Set<T> convertArrayToSet(T array[])
    {

        // Create the Set by passing the Array
        // as parameter in the constructor
        Set<T> set = new HashSet<>(Arrays.asList(array));

        // Return the converted Set
        return set;
    }
    public static void misingnumber(Integer[] nums)

    {
       Arrays.sort(nums);
        int min=nums[0];
        int max=nums[nums.length-1];
        Set<Integer> targetSet = convertArrayToSet (nums);
        Set<Integer> resultset=new HashSet<> ();
        System.out.println (targetSet);
       for(Integer i=min;i<=max;i++)
            resultset.add (i);
        Set<Integer> diff=new HashSet<> ();
             resultset.removeAll(targetSet);
        System.out.println (resultset);

       }




    public static void main(String[] args) {

                misingnumber (new Integer[]{1,5, 3, 4, 7});


    }
}

