# FinalProject#
Z-Score Calculator
This program is designed to take in user input and calculate the Z-Score, which can be done by plugging in the user's inputed values into an equation. This Z-Score is then used to find a specific value of a relatively large 2D array that contains the probability or "p-value" of the Z-Score that was inputted. This program is applicable in many different situations to do with statistics and math in general. 

### Difficulties or opportunities I encountered along the way.

The toughest part of this project was figuring out how to find the correct value in the 2D array as I had to mess around with the Z-Score value itself and then find the corresponding p-value from the 2D array. This resulted in some confusion as there were many different conditions so I had to utilize "if" and "for" loops to make sure that all conditions were met.

### Most interesting piece of my code and explanation for what it does.

Z=(Parameter-PopMean)/StandardDev;
Z=Math.round(Z * 100.0) / 100.0;
System.out.println("Your Z-Score is:"+Z);

if (Z<=-4) {
	System.out.println("Your P-Value is approximately 0\n");
}
else if (Z>=4) {
	System.out.println("Your P-Value is approximately 1\n");
}
else {
	double end;
	double front;
	double end1;
	double end2;

	double tester;
	Z=Z*100;
	
	end1=Math.abs(Z%10);
	end=Z%10;
	front=(Z-end)/10;
	int r=0;
	int c=0;
	for(int i=0;i<=Standard.length-1;i++) {
		if (Standard[i][0]==end1) {
		r=i;
		}
	
	
	for (int z=0;z<=Standard[0].length-1;z++) {
		if(Standard[0][z]==front) {
		c=z;
		}
	
	
	tester=Standard[r][c];
	}
	}
	System.out.println("Your P-Value is approximately "+Standard[r][c]);
}
This is the code that calculated the Z-Score and then calculated the p-value after getting that value. Modular division was utilized in order to chop off the end of the Z-Score and use that value to find the corresponding p-value in the 2D array. Many if and for loops were used to ensure that all conditions were met as there are multiple situations where the program would stop unexpectedly if all conditions were not met. 

## Built With

* [Eclipse](https://www.eclipse.org/ide/) - The IDE used

## Authors

* **Ammar Dameh** 

## Acknowledgments

* The values included in the Standard Distribution Table were collected from the University of Arizona

