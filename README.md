# Unexpected Behavior with instance_variable_set in Ruby

This repository demonstrates a potential issue when directly manipulating instance variables in Ruby using `instance_variable_set`. While functional, it's generally considered an uncommon and less-than-ideal practice.

**Problem:**
The example shows that modifying an instance variable directly using `instance_variable_set` bypasses any potential accessor methods or validation you might have in place. This can lead to inconsistencies in data management and makes it more difficult to track how data is modified within your class.

**Solution:**
The better solution is to use standard accessor methods (`attr_accessor`, `attr_reader`, `attr_writer`). These provide a centralized point of control over how instance variables are accessed and modified, improving code clarity, maintainability, and reducing the risk of unexpected issues.