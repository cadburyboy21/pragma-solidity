# pragma-solidity
Basic arithmetic operations

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract BasicOperations {
    // Define variables of different data types
    uint256 public num1;
    uint256 public num2;
    string public str1;
    string public str2;
    address public addr1;
    address public addr2;
    
    // Constructor to initialize variables
    constructor(uint256 _num1, uint256 _num2, string memory _str1, string memory _str2, address _addr1, address _addr2) {
        num1 = _num1;
        num2 = _num2;
        str1 = _str1;
        str2 = _str2;
        addr1 = _addr1;
        addr2 = _addr2;
    }
    
    // Function to perform arithmetic operations
    function performArithmeticOperations() public view returns (uint256, uint256, uint256, uint256) {
        uint256 addition = num1 + num2;
        uint256 subtraction = num1 - num2;
        uint256 multiplication = num1 * num2;
        uint256 division = num1 / num2;
        
        return (addition, subtraction, multiplication, division);
    }
    
    // Function to concatenate strings
    function concatenateStrings() public view returns (string memory) {
        string memory concatenated = string(abi.encodePacked(str1, str2));
        return concatenated;
    }
}
