---
description: >-
  User guide for the fixed rate, fixed term, no liquidation borrowing
  application
---

# Borrow App

**Moon Cake \(tentative name\) is a collateralized borrowing platform created by** [**PRL.one**](https://www.prl.one/)**. It offers users the ability to borrow cash, using their cryptocurrency holdings as collateral, at a fixed rate with no liquidation. This document will serve as a user guide, including a how-to guide and explanation about the protocol.** 

## **Deployment Details**

Current Status: Kovan testnet

Link to site: [borrow.prl.one](http://borrow.prl.one)

Current Supported Collateral: AMPL

Deployed addresses:

* AMPL 30 day bond: [0x8b3ea6492d25796346aa8a2c2e63da3e9e0ef75a](https://kovan.etherscan.io/address/0x8b3ea6492d25796346aa8a2c2e63da3e9e0ef75a)
* UNIv3 Loan Router: [0xc62c232cfbcf3f45c167a722e90dae3311c75de1](https://kovan.etherscan.io/address/0xc62c232cfbcf3f45c167a722e90dae3311c75de1)
* Testnet AMPL: [0x3e0437898a5667a4769b1ca5a34aab1ae7e81377](https://kovan.etherscan.io/token/0x3e0437898a5667a4769b1ca5a34aab1ae7e81377)
* Testnet USDT: [0xaff4481d10270f50f203e0763e2597776068cbc5](https://kovan.etherscan.io/token/0xaff4481d10270f50f203e0763e2597776068cbc5)

## How to Borrow with AMPL

The first action for the user is to specify the amount of USDT they want to borrow.   


![](https://lh3.googleusercontent.com/RwGNPnybv9v7D4MmtwSNFsmIT4opYZsUmvOrfvlYFBc2CYbc4Omli0rcVRjaduU29W7ldDzai6zVPIm7sxi62PHAkti_fQpvMV_pTygLKrU1Pf2_q8RN-6Q93bVS_yq0iWpn6-oT=s0)

After doing so, they will be greeted with a list of options to configure their loan.  


![](https://lh4.googleusercontent.com/-l_IoIkBFRj-NlQuTtypZU7RKAsJT-139JIIquKAa9-eYNjv3Hm_z5QIEViNFhmI2gR3t9Jxm0o9FfiJFAJd0kPBZXDTYVZ0GifeX1FX639KJ4eCMU895mlp0C-xL7-RzX-YiEu6=s0)

Options: 

* Borrow term: The length of time that they wish to borrow for. After this period is over, the borrower should come back to the app to repay their loan and get their collateral back - including any net positive value increase.
* Collateral amount: The user can select how much AMPL they want to use as collateral. As a general rule, more collateral will result in lower interest rate.

Once the user has selected their loan configuration, they click Deposit & Borrow to move on to the next step: approving the AMPL collateral:



![](https://lh4.googleusercontent.com/usAqrJD0zIFHo_7AySzr4SSoxOfdEC4gTqW6vWJxTKlJLuEV3xDuSNJEt44IhAUAtUSNZUNFUdl2ty5VhO_8m5DEb0rEh0xCAUGqTgnuLiMcRSOkbmB4--ZSpyPYh9CB3eXLx9_r=s0)

Their wallet will then pop up a transaction to approve the configured amount of collateral to the loan controller. Then they just have one more transaction to finish the loan:  


![](https://lh5.googleusercontent.com/gR9UZe3VcUBWJevUS0QVZ3kvNIgl-KRC6IDgLcCd-dLdP2TFDRL4PiUVn-h-ItFKlMtZepkeZHQX9kH_AtdD1WjwHASPM-PqqNeNch3syXzhZdQEEtHo30DU8Qkjq5TuEVJFx2zu=s0)

Once that transaction confirms, the loan has been created! The user’s USDT balance should have increased by their requested value:

![](https://lh4.googleusercontent.com/IETG3qXeXF6mPDcUZ7FdDzQbxjQ4tOTQO97zWGb0J3jCQufay5ti2mipSiP47sbnlIsWqspmGw5z3I-84DWZt-Iz8T1Tc1xX0YTtKhCc3NeaqpISu-P2R8TAI5TTpT8Lf1zELDk2=s0)

**You can find a video version of this demo** [**here**](https://www.loom.com/share/88e686e6f786429181265c9443c0e776)  
****

