# Boomi-Integtraion Get Route Key Header

![image](https://user-images.githubusercontent.com/97012694/147902617-8e44191c-ddbd-4fa3-a17c-b7a0da269ec9.png)

We need to get the header out of it as a route key(eg: CreateVoyageRequest) . This acts as a routing parameter for different types of header such as UpdateteVoyageRequest , DeleteVoyageRequest,etc.

So, we need to add a script and data process for route key

![image](https://user-images.githubusercontent.com/97012694/147902808-4cdc51f0-1cea-4498-9c41-3256d04b2a8b.png)

1st step is search and replace: Text to Find- **<\?xml.*\?>** Replace with space

![image](https://user-images.githubusercontent.com/97012694/147902837-1a7f0aec-906c-4975-a01b-8d5a364904b5.png)

2nd Step is Scripting in groovy
//This script strips the first line out of each document and outputs the rest of the document contents unaltered.
Find the script in 1stfile

3rd step is Scripting in groovy
// This script reads the first line out of each document and outputs only that line, ignoring the remaining lines.
Find the script in 2ndfile

4th step is search and replace: Text to Find- **[^a-zA-Z0-9_-] ** Replace with space


5th step is search and replace: Text to Find- **ns0 ** Replace with space



Input and output screenshots

Input
![image](https://user-images.githubusercontent.com/97012694/147903103-357e2167-ed5a-44d7-a346-7c5e8386df3a.png)

Output

![image](https://user-images.githubusercontent.com/97012694/147903135-fc840502-81d3-4d27-aff8-3da4cb333c4d.png)


Full process Screenshot

![image](https://user-images.githubusercontent.com/97012694/147903180-2f6ca566-2a7f-46f2-bfc2-cd0c7e68691d.png)


