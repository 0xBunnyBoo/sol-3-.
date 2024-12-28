// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC1155/ERC1155.sol";

contract MyMultiToken is ERC1155 {
    constructor() ERC1155("https://api.example.com/metadata/{id}.json") {
        _mint(msg.sender, 0, 1000, ""); // توکن ID 0 با مقدار 1000
        _mint(msg.sender, 1, 500, "");  // توکن ID 1 با مقدار 500
    }
}
