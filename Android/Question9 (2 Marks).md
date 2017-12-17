# Question 9 (C++)


Implement an intarator for the follwing data structure: 
```cpp
#include <iostream>
#include <vector>
#include <cstring>

class Tree {
public:
    // Set up the stuff they give us
    Tree(int val) {
        this->val = new int(val);
    }

    // Kill all the heap stuff
    ~Tree() {
        delete left;
        delete right;
        delete val;
    }


    void insert(int value) {
        // Deref the current value 
        int currVal = *val;
    

        if (value < currVal) {
            // Insert to the right
            // Determine if the right side has any set value
            if (right == nullptr) {
                right = new Tree(value);
            } else {
                // Get the right to insert ut
                right->insert(value);
            }
        } else {
            // Insert to the left
            
            // Determine if the left side has an existing value
            if (left == nullptr) {
                left = new Tree(value);
            } else {
                // Get the left to insert it
                left->insert(value);
            }
        }
    }



    // Getters
    Tree* getLeft(){return this->left;}
    Tree* getRight(){return this->right;}
    int getVal(){return *val;}


    // Function that allows you to traverse an entire tree
    std::vector<int> traverse() {
        std::vector<int> list(0);

        // If it is a terminating node
        if (getLeft() == nullptr && getRight() == nullptr) {
            list.push_back(*val);
            return list;        
        } else if (getRight() != nullptr) { 
            // Iterate over the left and right side
            // First over the right side

            // Transeverse the right
            // Append the transverese
            std::vector<int> rightTransverse(0);
            // Set the val
            rightTransverse = getRight()->traverse();
            list = rightTransverse;
        }

        list.push_back(*val);

        if (getLeft() != nullptr) {
            // Iterate over the left side

            // Transvered the left
            // Append transverse
            std::vector<int> leftTransverse(0);
            // Bop it
            leftTransverse = getLeft()->traverse();
            list.insert(list.end(), leftTransverse.begin(), leftTransverse.end());
        }

        return list;
    }


    // Insert function that allows you to insert one tree into another
    void add(Tree *treeTwo) {
        // Traverse the first tree
        // Insert each of the traveresd nodes individually
       std::vector<int> finTravered(0);
       finTravered = treeTwo->traverse();


        // Iterate over and insert
        for (int i: finTravered) {
            insert(i);
        }
    }




private:
    Tree *left = nullptr;
    Tree *right = nullptr;   
    int *val = nullptr; 
};
```
