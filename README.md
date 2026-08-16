// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract BidLog {
    uint256 public lastBid;

    function bid(uint256 amount) external {
        lastBid = amount;
    }
}
