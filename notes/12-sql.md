# SQL

Wednesday October 11th Auth0 with SQL

Post It SHARP
Allspice reference

foreign key constraint(This field relies on another table)
  FOREIGN KEY (creatorID) REFERENCES accounts(id) ON DELETE CASCADE
    creatorId - in this table id : - in the other table
                          
return edits in the service layer