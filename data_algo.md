2019/05/02 , mauroData Structures :Linked List Linear Collection of elements in which their order is not given by their memory location, the elements point to each other. taken from sourceCharacteristics :
	1. Insertion is O(1)
	2. Deletion is O(n)
	3. Searching is O(n)

Implementation//mauricio.rios@titoma.com#include <stdio.h>#include <stdint.h>#include <string.h>#include <stdlib.h>struct node {    int data;
	struct node *next ;
   	};
   	int main(void) {    struct node *Head;
    	struct node *new_node;
		struct node *traverse_node ;
	    	uint8_t node_counter = 0;
			Head = (struct node *)malloc (sizeof (struct node) );
		    	if (Head == NULL) {        printf("Error, can't allocate new node\r\n");
				return 0;
					}    Head->next = 0;
				    	Head->data = 1;
						new_node = (struct node *)malloc (sizeof (struct node) );
					    	if (new_node == NULL) {        printf("Error, can't allocate new node\r\n");
							return 0;
								}    Head->next= new_node;
							    	new_node->data = 2;
									new_node->next = NULL;
								    	/*Traverse list*/    traverse_node = Head;
										while (1) {        if (traverse_node == NULL){            printf("End of node was reached \r\n");
									    	break;
												}        printf("Current node %d ,data %d \r\n", node_counter++,traverse_node->data);
													traverse_node = traverse_node->next;
														}    return 0;
													   	}Multi-purpose Linked ListRather than having a predetermined data type we use void for the data type, in this manner we can stored any type of data (char, structures..)in the multi-purpose linked list struct node {    void *data;
													    	struct node *next ;
														};
														struct *node new_node ;
														/* Allocate char data*/new_node->data = malloc(n_elements*sizeof(char));
														/* Allocate int data*/new_node->data = malloc(n_elements*sizeof(int));
														Hashing functionMaps data of arbitrary size on to fixed size. They are used with hash table .source   Table creation

		1. Define the hash function, which return a index number , the functions shall be defined in the way that max index  is the max size of the table
		2. take input data and find it's hash value(hash table index/key)
		3. allocate the input data in the table [ key], hash collition can take place since two or more input values can generated the same hash to avoid thiswe can implement chaining or  open addressing

    Characteristics Space         O(n)[1]     O(n)Search        O(1)         O(n)Insert          O(1)         O(n)Delete         O(1)         O(n)
