public class InsertInMid {  
    //Represents the node of list.  
        public class Node{  
            int data;  
            Node next;  
            public Node(int data) {  
                this.data = data;  
            }  
        }  
  
        public int size;  
        //Declaring head and tail pointer as null.  
        public Node head = null;  
        public Node tail = null;  
  
        //This function will add the new node to the list.  
        public void add(int data){  
            //Create new node  
            Node newNode = new Node(data);  
            //Checks if the list is empty.  
            if(head == null) {  
                 //If list is empty, both head and tail would point to new node.  
                head = newNode;  
                tail = newNode;  
                newNode.next = head;  
            }  
            else {  
                //tail will point to new node.  
                tail.next = newNode;  
                //New node will become new tail.  
                tail = newNode;  
                //Since, it is circular linked list tail will points to head.  
                tail.next = head;  
            }  
            //Size will count the number of element in the list  
            size++;  
        }  
  
        //This function will add the new node at the middle of the list.  
        public void addInMid(int data){  
            Node newNode = new Node(data);  
            //Checks if the list is empty.  
            if(head == null){  
                //If list is empty, both head and tail would point to new node.  
                head = newNode;  
                tail = newNode;  
                newNode.next = head;  
            }  
            else{  
                Node temp,current;  
                //Store the mid-point of the list  
                int count = (size % 2 == 0) ? (size/2) : ((size+1)/2);  
                //temp will point to head  
                temp = head;  
                current= null;  
                for(int i = 0; i < count; i++){  
                    //Current will point to node previous to temp.  
                    current = temp;  
                    //Traverse through the list till the middle of the list is reached  
                    temp = temp.next;  
                }  
  
                //current will point to new node  
                current.next = newNode;  
                //new node will point to temp  
                newNode.next = temp;  
            }  
            size++;  
        }  
  
        //Displays all the nodes in the list  
        public void display() {  
            Node current = head;  
            if(head == null) {  
                System.out.println("List is empty");  
            }  
            else {  
                 do{  
                    //Prints each node by incrementing pointer.  
                    System.out.print(" "+ current.data);  
                    current = current.next;  
                }while(current != head);  
                System.out.println();  
            }  
        }  
  
        public static void main(String[] args) {  
            InsertInMid cl = new InsertInMid();  
            //Adds data to the list  
            cl.add(1);  
            cl.add(2);  
            cl.add(3);  
            cl.add(4);  
  
            System.out.println("Original list: ");  
            cl.display();  
  
            //Inserting node '5' in the middle  
            cl.addInMid(5);  
            System.out.println( "Updated List: ");  
            cl.display();  
  
            //Inserting node '6' in the middle  
            cl.addInMid(6);  
            System.out.println("Updated List: ");  
            cl.display();  
        }  
}
