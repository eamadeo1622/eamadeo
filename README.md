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
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract APRStorage {
    uint256 public apr; // in basis points

    function setAPR(uint256 _apr) external {
        apr = _apr;
    }
}
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract TokenURI {
    mapping(uint256 => string) public tokenURI;

    function setURI(uint256 tokenId, string calldata uri) external {
        tokenURI[tokenId] = uri;
    }
}
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract SafeTransferFlag {
    bool public safeMode = true;

    function setSafeMode(bool enabled) external {
        safeMode = enabled;
    }
}
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract RoyaltyReceiver {
    address public receiver;

    function setReceiver(address _receiver) external {
        receiver = _receiver;
    }
}
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract OfferAccepted {
    mapping(uint256 => bool) public accepted;

    function accept(uint256 tokenId) external {
        accepted[tokenId] = true;
    }
}
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract PublicMint {
    bool public publicMintEnabled;

    function enablePublicMint() external {
        publicMintEnabled = true;
    }
}
