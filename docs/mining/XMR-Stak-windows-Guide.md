# **How to Set Up XMR-Stak for Windows**

XMR-Stak is a unified miner, which means the same program will be used to mine with both your CPU and your GPU. It will automatically detect your hardware and adjust the settings accordingly.

## **Downloading and Installing**

1. Download and install [XMR-Stak Unified Miner](https://github.com/fireice-uk/xmr-stak/releases/latest). It will auto-detect your hardware, and tune everything for you.
2. Make a folder called `TurtleCoin Miner` on your Desktop and unzip the files you just downloaded for XMR-Stak in there.
3. Double-click on `xmr-stak.exe`.

    #### To start XMR-Stak without using your CPU/GPU, follow these steps <a name= "#xmr-stak-no-cpu-gpu"> </a>

    - Open Command Prompt

    - Type `cd Desktop\TurtleCoin Miner`

    - To start XMR-Stak without utilising the CPU, type `xmr-stak.exe --noCPU`
    - To start XMR-Stak without utilizing your nVidia GPU, type `xmr-stak.exe --noNVIDIA`
    - To start XMR-Stak without utilizing your AMD GPU, type `xmr-stak.exe --noAMD`
    - To start XMR-Stak without utilizing either of your GPU's, type `xmr-stak.exe --noAMD --noNVIDIA`

    **If you want to use both your CPU and your GPU, ignore these steps. Just launch `xmr-stak.exe`**

4. Click `Yes` when it asks if you want to run as Administrator. This is so that the program can see what hardware you're running.
5. Check [XMR-Stak Setup and Configuration](#setup-and-config)

## **XMR-Stak Setup and Configuration**<a name="setup-and-config"></a>

Upon first launching XMR-Stak, the software will ask you several setup and configuration questions.

1.  `Please enter: - Do you want to use the HTTP interface? Unlike the screen display, browser interface is not affected by the GPU lag. If you don't want to use it, please enter 0, otherwise enter port number that the miner should listen on`


    Enter `0`, if you do not need to remotely check your hashrate.

    If you do need to, then enter a port number.
    Let's take the port number as `16000` and your IP address as `88.20.105.14` as an example.

    To check the hashrate, enter in the address bar of your web browser, `<88.20.105.14>:<0101>`. It should show a page with your rig's hashrate.  
    If you are checking from the same IP address, you can alternatively enter, `localhost:<0101>`

    Make sure to enter your own IP address if you enable this feature. You can choose any port you want!

2.  
   ```
    Please enter:

    - Please enter the currency that you want to mine: 
	- aeon7
	- bbscoin
	- bittube
	- cryptonight
	- cryptonight_bittube2
	- cryptonight_masari
	- cryptonight_haven
	- cryptonight_heavy
	- cryptonight_lite
	- cryptonight_lite_v7
	- cryptonight_lite_v7_xor
	- cryptonight_v7
	- cryptonight_v8
	- cryptonight_v7_stellite
	- graft
	- haven
	- intense
	- masari
	- monero
	- qrl
	- ryo
	- stellite
	- turtlecoin

   ```

    Enter `cryptonight_haven`

3.  `- Pool address: e.g. pool.example.com:3333 `

    Choose a pool from any of the [available pools](https://bloc.money/mining) that is **closest to you** and enter its URL (you will be able to add more later).

4.  `- Username (Wallet address or pool login):`  

    If you have not yet downloaded and ran the BLOC software to sync the blockchain and create a wallet, you can [create your wallet](../../wallets/Making-a-Wallet) before start mining.

5.  `- Password (mostly empty or x):`  

    Leave it empty and press enter.

6.  `- Rig identifier for pool-side statistics (needs pool support). Can be empty:`

    Leave it empty and press enter.

7.  `- Does this pool port support TLS/SSL? Use no if unknown. (y/N)`  

    In most cases, `N` is fine.

8.  `- Do you want to use nicehash on this pool? (y/n)`  

    Enter `n`(in case you do, enter `y`).

9.  `- Do you want to use multiple pools? (y/n)`  

    * Enter `y` if you would like to add more pools.
    * Give them all a weight of `10` if you're tired of reading, or if you want the best experience, give the pools nearest to you a higher number, and the ones further from you a lower number.  
    * XMR-Stak will prioritize the highest weight pool, and fall back to the others if it cannot connect.
    * If they are all given the same weight, it will connect to them in order of how they are listed, form top to bottom, in the configuration file.
    * If you are on Windows 7/8, it will ask for administrator permission again. Click `Yes` to grant it permission.
    * If you are on Windows 10, it will not ask for it again.


Done! The miner will now start scanning your hardware and will begin mining. Awesome!

XMR-Stak will save your configuration in `config.txt`  in the same directory from which it was first run.

Your configuration for pools(algorithm to mine, address, port etc) will be saved in `pools.txt`
The configuration of the device it mines(CPU/AMD/NVIDIA) will be saved in `cpu.txt`, `amd.txt` or `nvidia.txt`, respectively.

Run XMR-Stak again from the same directory to reuse the configuration.