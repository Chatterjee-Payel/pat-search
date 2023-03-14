# pat-search
class Solution{
public:	
	
	int search(string text, string pat)
	{
	    // Your code goes here
	   int j=0;
	   int i=0;
	   string temp;
	   int n=text.size();
	   int k=pat.size();
	  while(j<n)
	  {
	      if(j-i+1<k)
	      {
	          temp.push_back(text[j]);
	          j++;
	      }
	      else
	          if(j-i+1==k)
	          {
	              temp.push_back(text[j]);
	              if(pat==temp)
	              {
	                  return 1;
	              }
	              temp.erase(temp.begin());
	              i++;
	              j++;
	          }
	      
	  }
	  return 0;
	}
};
