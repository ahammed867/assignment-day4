# assignment-day4
report card
//DETAILS


Transaction Hash:
0x9e5d9d53df8d8badce29c86337e143566e3c8e5a0290ed557327610fe9bf1fb1 
Status:
Success
Block:
3132631 2 Block Confirmations
Timestamp:
34 secs ago (Jul-29-2020 06:05:14 PM +UTC)
From:
0xfc059bec1945aae7552282684f4e65ae03e37c46 
To:
[Contract 0xe191166613bd78f6dfd502a441b6ff661ff36409Created] 
Value:
0 Ether ($0.00)
Transaction Fee:
0.000176023 Ether ($0.000000)




pragma solidity 0.6.6;
  
  
  
contract reportCard{
    bytes32 name;
    uint rollnumber;
    bytes32 batch;
    uint marks1;
    uint marks2;
    uint marks3;
    uint marks4;
    uint result;
    bytes32 status;
    
    function reportcard(bytes32 name1, uint rollno1, bytes32 batch1, uint marksq1, uint marksq2, uint marksq3, uint marksq4 ) public {
        
        name = name1;                          
        rollnumber = rollno1;
        batch = batch1;
        marks1 = marksq1;
        marks2 = marksq2;
        marks3 = marksq3;
        marks4 = marksq4;
        
        result = marks1 + marks2 + marks3 + marks4;
        result = result * 100/400;
        
         if( result < 40){
            status = "fail";
         }
        else(result >= 40);{
            status = "pass";
        }
    }
    
    function getdetails() public view returns(bytes32, uint, bytes32, uint, uint, uint, uint, uint, bytes32){
        return (name, rollnumber, batch, marks1, marks2, marks3, marks4, result, status);
    }
}
  
