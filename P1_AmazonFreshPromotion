
public class P1_AmazonFreshPromotion {

//	------------- Problem 1 ----------------
//	Amazon Fresh is running a promotion in which customers receive prizes for purchasing a secret combination of fruits. 
//	The combination will change each day, and the team running the promotion wants to use a code list to make it easy to change the combination. 
//	The code list contains groups of fruits. Both the order of the groups within the code list and the order of the fruits within the groups matter. 
//	However, between the groups of fruits, any number, and type of fruit is allowable. The term "anything" is used to allow for any type of fruit to appear 
//	in that location within the group.Consider the following secret code list: [[apple, apple], [banana, anything, banana]]
//	Based on the above secret code list, a customer who made either of the following purchases would win the prize:
//	orange, apple, apple, banana, orange, banana
//	apple, apple, orange, orange, banana, apple, banana, banana
//	Write an algorithm to output 1 if the customer is a winner else output 0.
//
//	------- Input --------------
//	The input to the function/method consists of two arguments:
//	codeList, a list of lists of strings representing the order and grouping of specific fruits that must be purchased in order to win the prize for the day.
//	shoppingCart, a list of strings representing the order in which a customer purchases fruit.
	
//	--------- Output ------------------
//	Return an integer 1 if the customer is a winner else return 0.
//	Note
//	'anything' in the codeList represents that any fruit can be ordered in place of 'anything' in the group. 'anything' has to be something, it cannot be "nothing."
//	'anything' must represent one and only one fruit.
//	If secret code list is empty then it is assumed that the customer is a winner.
	
//	Example 1
//	-----------------------------
//	Input 
//	codeList = [[apple, apple], [banana, anything, banana]] shoppingCart = [orange, apple, apple, banana, orange, banana]
//	Output: 1
	
//	Example 2
//	-----------------------------
//	Input 
//	codeList = [[apple, apple], [banana, anything, banana]] shoppingCart = [banana, orange, banana, apple, apple]
//	Output: 0
	
//	Example 3
//	-----------------------------
//	Input 
//	codeList = [[apple, apple], [banana, anything, banana]] shoppingCart = [apple, banana, apple, banana, orange, banana]
//	Output: 0
	
//	Example 4
//	-----------------------------
//	Input 
//	codeList = [[apple, apple], [apple, apple, banana]] shoppingCart = [apple, apple, apple, banana]
//	Output: 0	
	
	public static void main(String[] args){
		
        String[][] codeList1 = { { "apple", "apple" }, { "banana", "anything", "banana" } };
        String[] shoppingCart1 = {"orange", "apple", "apple", "banana", "orange", "banana"};
        
        String[][] codeList2 = { { "apple", "apple" }, { "banana", "anything", "banana" } };
        String[] shoppingCart2 = {"banana", "orange", "banana", "apple", "apple"};
        
        String[][] codeList3 = { { "apple", "apple" }, { "banana", "anything", "banana" } };
        String[] shoppingCart3 = {"apple", "banana", "apple", "banana", "orange", "banana"};
        
        String[][] codeList4 = { { "apple", "apple" }, { "apple", "apple", "banana" } };
        String[] shoppingCart4 = {"apple", "apple", "apple", "banana"};
        
        
        System.out.println(check(codeList1,shoppingCart1));
        System.out.println(check(codeList2,shoppingCart2));
        System.out.println(check(codeList3,shoppingCart3));
        System.out.println(check(codeList4,shoppingCart4));
        
	}
	
	private static int check(String[][] codeList,String[] shoppingcart){
		
		// check corner cases
		if(codeList == null || codeList.length == 0) return 1;
		if(shoppingcart == null || shoppingcart.length == 0) return 0;
		
		int i =0,j=0;
		
		while(i<codeList.length && j+codeList[i].length <= shoppingcart.length){
			
			boolean match = true;
			
			for(int k = 0;k<codeList[i].length;k++){
				
				if(!codeList[i][k].equals("anything") && !shoppingcart[j+k].equals(codeList[i][k])){
					match = false;
					break;
				}
			}
			
			if(match){
				j+= codeList[i].length;
				i++;
			}else{
				j++;
			}
		}
		
		return (i == codeList.length)?1:0;
	}
	

}
