# finding-Second-largest-element-in-a-array
Finding second largest element in Array
Description: we need to find the second largest element in array so we have to write efficient solution which having very less time complexity.
Input array:
10	50	45	47	38

Output:
     47 is  second largest element.
Let see solution:
# Naïve Solution:
    In that first we find first largest element and then we find second largest so we traverse loop in such way if it is not first largest element we go inside if block and do finding second largest element.
   
   #############################################
   int second(int a[],size){
   int largest=largestelement(a,size);
    int res=-1;
   For(int i=0;i<size;i++){
        If(a[largest]!=a[i]){
          If(res==-1)  {
                res=i;}
          else If(a[res]<a[i]){
                    res=i;
}}
}
    Return res;}
###################################################
 

Int  largestelement(int a[],int size){
  int res=0;
 For(int i=1;i<size;i++){
     If(a[res]<a[i]){
          res=i;
}
   Return res;

}
}
###################################################

So this is two traversal solution with time complexity O(n)


# Efficient Solution: In one traversal
We do only one traversal and in that we use to find fist largest so with that we also keep track of second largest
.
int second(int a[],size){
  int res=-1;
  int largest=0;
   For(int i=1;i<size;i++){
        If(a[largest]<a[i]){
           res=largest;
            largest=i;}
          else if(a[largest]!=a[i])  {
              if(res==-1)
                res=i;}
                else If(a[res]<a[i]){
                    res=I;
}}
}
    Return res;}
	

//Most of the beginner thing why we are writing else if condition. So by using that only your output   come because it imagine array like 4,6,3,2 or 4,5,6,7   So they thing like that but if we write only if condition it only work for sorted So, of unsorted array we have to write both condition. Think if we have array like 4,7,5,6 so in that case both condition should write must.
