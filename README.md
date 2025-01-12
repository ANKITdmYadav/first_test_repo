int singleNonDuplicate(vector<int>& nums) {
        int n=nums.size();
        int low=0;
        int high=n-1;
        int mid;
        while(low<high){
            mid=(low+high)/2;
            if(nums[mid]==nums[mid+1]){
                mid+=1;
            }
            if((mid-low)%2!=0){
                low=mid+1;
            }
            else
            high=mid-1;
        }
        return nums[low] ;
    }
