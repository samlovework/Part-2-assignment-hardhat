# Part-2-assignment-hardhat

import { ethers } from 'hardhat';

async function main() {
    const nft = await ethers.deployContract('Counter');

    await nft.waitForDeployment();

    console.log('NFT Contract Deployed at ' + nft.target);
}

// We recommend this pattern to be able to use async/await everywhere
// and properly handle errors.
main().catch((error) => {
    console.error(error);
    process.exitCode = 1;
});
// 0xC67205bdF375894C0f3BCc106F01592549Fe8D06
