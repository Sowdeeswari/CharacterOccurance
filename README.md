# CharacterOccurance
import java.util.Iterator;
import java.util.LinkedHashMap;
import java.util.Map;
import java.util.Set;

public class CharacterOccurance {
public static void main(String[] args) {
		String s = "java is easy";
		Map<Character,Integer> m = new LinkedHashMap<Character,Integer>();
		for (int i = 0;i<s.length();i++) 
		{
			if(m.get(s.charAt(i))==null)
			{
				m.put(s.charAt(i),1);
			}
			else
			{
				int count = m.get(s.charAt(i));
				m.put(s.charAt(i), count++);
			}	
		}
		Set<Character> s2= m.keySet();
		Iterator<Character> i = s2.iterator();
		while(i.hasNext()) {
			char ch = i.next();
		System.out.println(ch+" "+m.get(ch));
	}
}
}
