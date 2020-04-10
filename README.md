# upload-1
operating system
#include<stdio.h>
main()
{
	int n,f,j,i,z,disp;
	int flag=0;
	int pf=0,a=0;
	int fr[10],s[100];
	printf("Enter no. of pages");
	scanf("%d",&n);
	printf("Enter no. of frames");
	scanf("%d",&f);
	for(i=0;i<f;i++)
		fr[i]=-1;
		printf("Enter reference string \n");
	for(i=0;i<n;i++)
	 {
	 scanf("%d",&s[i]);}
	for(z=0;z<n;z++)
	{
		a=0;
		for(j=0;j<f;j++)
		{
			if(s[z]==fr[j])
			a++;
		}
		if (a==0)
		{
			fr[flag]=s[z];
			flag++;
		pf++;	
		}
		if(flag>(f-1))
		flag=0;
		printf("%d------->",s[z]);
		for(disp=0;disp<f;disp++)
        printf("%d \t",fr[disp]);
        printf("\n");
	 } 
		printf("page fault: %d",pf)	;
}
