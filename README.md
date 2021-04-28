# vector-code
additing two vector and storing them n 3rd one 
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text; 

namespace HelloWorld 
   {
            class Program
            {
 	static void Main(string[] args)
	{
                               Console.WriteLine("Enter the length of arrays: ");
                                int l = Convert.ToInt32(Console.ReadLine());
                                Console.WriteLine("Length of arrays: {0}", l); 

                                string[] real1 = new string[l]; string[] imag1 = new string[l];
                                string[] real2 = new string[l]; string[] imag2 = new string[l]; 

                                 int[] real3 = new int[l];
                                 int[] imag3 = new int[l];
                                 double[] y = new double[l];
                                 double[] z = new double[l]; 

                                string[] vector3 = new string[l];
                                string[] v3_mag = new string[l];
                                string[] v3_phase = new string[l];
                                string[] v3_mag_phase = new string[l]; 

                                 string[] a = new string[l];
                                 string[] b = new string[l];
                                 string[] c = new string[l];
                                 string[] d = new string[l];
                                 string[] e = new string[l];
                                 string[] f = new string[l];
                                 string[] g = new string[l]; 


Console.WriteLine("\n==============================================");
Console.WriteLine("=========== For Vector 1 =====================");
Console.WriteLine("==============================================");
for (int j = 0; j < l; j++)
{

Console.WriteLine("Enter {0} Real entry: ", j + 1);
string r1 = Console.ReadLine();
real1[j] = r1;

Console.WriteLine("Enter {0} Imaginary entry: ", j + 1);
string i1 = Console.ReadLine();
imag1[j] = i1;
a[j] = i1 + 'i';
}

Console.WriteLine("\n==============================================");
Console.WriteLine("=========== For Vector 2 =====================");
Console.WriteLine("==============================================");
for (int k = 0; k < l; k++)

{

Console.WriteLine("Enter {0} Real entry: ", k + 1);
string r2 = Console.ReadLine();
real2[k] = r2;

Console.WriteLine("Enter {0} Imaginary entry: ", k + 1);
string i2 = Console.ReadLine();
imag2[k] = i2;

                          b[k] = i2 + 'i';
	}

	Console.WriteLine("\n==============================================");
	Console.WriteLine("======= Display of Vector 1 & Vector 2 ======="); 	Console.WriteLine("==============================================");
	for (int p = 0; p < l; p++)

	{

	c[p] = real1[p] + '+' + a[p];
		d[p] = real2[p] + '+' + b[p]; 	
                 }
                                             Console.WriteLine("Vector 1: ");
                                             Console.WriteLine("[{0}]", string.Join(", ", c));
                                             Console.WriteLine("\nVector 2: ");
                                             Console.WriteLine("[{0}]", string.Join(", ", d)); 

// Addition of Vector 1 & Vector 2
                                               for (int q = 0; q < l; q++)
              {

                                        real3[q] = Convert.ToInt32(real1[q]) + Convert.ToInt32(real2[q]);
                                                       e[q] = Convert.ToString(real3[q]);
                                                    imag3[q] = Convert.ToInt32(imag1[q]) + Convert.ToInt32(imag2[q]);
                                                   f[q] = Convert.ToString(imag3[q]);

		g[q] = f[q] + 'i'; 
                                            }

	Console.WriteLine("\n==============================================");
	Console.WriteLine("==== Displays of Vector 3 after addition ====="); 	Console.WriteLine("==============================================");


	for (int r = 0; r < l; r++)
	{
                       vector3[r] = e[r] + '+' + g[r];
                }
                                               Console.WriteLine("\nSimple Complex Vector 3 Display");
                                                 Console.WriteLine("[{0}]", string.Join(", ", vector3)); 
                  for (int r = 0; r < l; r++)
                {


                                              // For Magnitudes
                                                           double aa = Convert.ToDouble(real3[r]);
                                                           double bb = Convert.ToDouble(imag3[r]);
                                                           double cc = (aa * aa) + (bb * bb);
                                            y[r] = Math.Round(Math.Sqrt(cc), 4);
                                            v3_mag[r] = Convert.ToString(y[r]); 


                                                // For Phase in degrees
                                                          double dd = bb / aa;
                                                          double ee = Math.Atan(dd);
                                                          double ff = ee * (180 / Math.PI);
                                           z[r] = Math.Round(ff, 2);
                                          v3_phase[r] = Convert.ToString(z[r]); 

                                         // For combined Magnitude & Phase
                                         v3_mag_phase[r] = v3_mag[r] + '<' + v3_phase[r];
	      }

                                               Console.WriteLine("\nMagnitude display of Vector 3");
                                               Console.WriteLine("[{0}]", string.Join(", ", v3_mag));
                                               Console.WriteLine("\nPhase (in deg) display of Vector 3");
                                               Console.WriteLine("[{0}]", string.Join(", ", v3_phase));
                                               Console.WriteLine("\nMagnitude & Phase display of Vector 3");
                                               Console.WriteLine("[{0}]", string.Join(", ", v3_mag_phase));
                                               Console.WriteLine("\n");
	 }
	 }
	 }


