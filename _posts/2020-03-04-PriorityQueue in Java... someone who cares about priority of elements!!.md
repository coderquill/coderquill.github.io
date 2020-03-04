Priority queue is a data structure which stores data according to its priority. 
What it means is when elements will be accessed from the said priority queue, they will be pulled out according to their priority.
Applications:
To implement heap.(Min heap as well as max heap)

Code:
Declaration:
PriorityQueue<contentType> name = new PriorityQueue<contentType>();
the above type of queue will have priority decided as descending order.

If we want the priority of the priority queue to be in ascending order, we can do it by writing our own comparator.
It can be done as follows:
class The_Comparator implements Comparator<Integer>{
  pulic int compare(Integer a, Integer b){
      return a-b;
  }
}
class example{
  public static void main(String args[]){
      PriorityQueue<Integer> pq = new PriorityQueue<Integer>(new The_Comparator());
      pq.add("10");
      pq.add("5");
      pq.add("15");
      while(!pq.isEmpty()){
        System.out.println(pq.poll());
      }
  }
}

Output:
5
10
15
