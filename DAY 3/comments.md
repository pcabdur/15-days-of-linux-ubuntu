#!/bin/bash

echo "Creating a test file..."
touch test.txt

echo "Changing ownership to root..."
sudo chown root:root test.txt
ls -l test.txt

echo "Giving it back to myself..."
sudo chown $USER:$USER test.txt
ls -l test.txt
