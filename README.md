// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract BidLog {
    uint256 public lastBid;

    function bid(uint256 amount) external {
        lastBid = amount;
    }
}
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract ContributionTracker {
    mapping(address => uint256) public contributions;

    function contribute() external payable {
        contributions[msg.sender] += msg.value;
    }
}
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract StakingWithdraw {
    mapping(address => bool) public canWithdraw;

    function enableWithdraw() external {
        canWithdraw[msg.sender] = true;
    }
}
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract APRStorage {
    uint256 public apr; // in basis points

    function setAPR(uint256 _apr) external {
        apr = _apr;
    }
}
