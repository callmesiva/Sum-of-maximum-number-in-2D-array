# Sum-of-maximum-number-in-2D-array

        int arr [] [] = {{1,2,10},
                        {4,5,10},
                        {7,8,9}};
       
        int rowval=Integer.MIN_VALUE;
        int colval=Integer.MIN_VALUE;
        int rightdaigonal=Integer.MIN_VALUE;
        int rightsum=0;
        int leftdaigonal=Integer.MIN_VALUE;
        int leftsum=0;
       
       
      for(int i=0; i<arr.length; i++)   // find big in row
      {
        int sum=0;
        for(int j=0; j<arr[i].length; j++)
        {
          sum= sum+arr[i][j];
          
          if(sum>rowval)
          {
            rowval=sum;
          }
          
        }
      }
       System.out.println("Sum of row is : " +rowval);
       
       for(int i=0; i<arr.length; i++) // find big in col
       {
         int sum=0;
         for(int j=0; j<arr[i].length; j++)
         {
           sum=sum+arr[j][i];
           if(sum>colval)
           {
             colval=sum;
           }
         }
       }
      System.out.println("Sum of column is : " +colval);
      
   
       for(int i=0;  i<arr.length; i++)
      {
       
        for(int j=i; j<=i; j++)
        {
          rightsum= rightsum+arr[i][j];
        
          if(rightsum>rightdaigonal)
          {
           rightdaigonal=rightsum;
          }
        }
      }
      System.out.println("Sum of right daigonal is : " +rightdaigonal);
      
      for(int  i=0; i<arr.length; i++)
       {
         for(int j=arr.length-(i+1); j>=arr.length-(i+1); j--)
         {
           leftsum= leftsum + arr[i][j];
           if(leftsum>leftdaigonal)
           {
             leftdaigonal=leftsum;
           }
         }
       }
     
     System.out.println("Sum of left daigonal is : "+leftdaigonal);
     
     
      int m1  = rowval>colval ? rowval:colval;
      
      int m2 = rightdaigonal>leftdaigonal? rightdaigonal:leftdaigonal;
      
      int max= m1>m2?m1:m2;
      
      System.out.print("Sum of maximum number in 2D array is : "+max);
