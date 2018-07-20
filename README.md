import java.util.Scanner;

public class afrequency {

	public static void main(String args[]){
  
		Scanner sys = new Scanner (System.in);
    
		int count=0;
		
		System.out.println("Enter The Size of the Array : ");
		int num = sys.nextInt();
		
		int arr[] = new int[num];
		
		System.out.println("Enter The Elements in the array : ");
		for(int i=0;i<num;i++){
			arr[i] = sys.nextInt();
		}		
		
		for(int i=0;i<num;i++){
			count=1;
			for(int j=i+1;j<num;j++){
				if(arr[i]==arr[j] && arr[i]!='\0'){
					count++;
					arr[j]='\0';
				}
			}
      
			if(arr[i]!='\0'){
				System.out.println(arr[i] +" Appears "+count+" Times.");
			}
      
		}	
		
    
	}
}
