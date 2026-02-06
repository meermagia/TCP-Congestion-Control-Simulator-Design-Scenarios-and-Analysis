# TCP Congestion Control Simulator

This project is a Python-based, event-driven simulator designed to analyze and compare the performance of various TCP congestion control algorithms, including **TCP Reno**, **TCP Cubic**, and **TCP BBR**.

The simulator runs within a Jupyter Notebook and visualizes key metrics such as throughput, Round Trip Time (RTT), and fairness (Jain's Index) across different network conditions.

## Features

* **Event-Driven Simulation:** Accurate simulation of packet transmissions, acknowledgments (ACKs), timeouts, and drops.
* **Congestion Control Algorithms:**
    * **Reno:** Standard loss-based congestion control.
    * **Cubic:** The default Linux congestion control, optimized for high-bandwidth-delay product networks.
    * **BBR:** Google's congestion-based congestion control that models bandwidth and RTT.
* **Network Models:**
    * **Link Characteristics:** Configurable bandwidth, propagation delay, and buffer size.
    * **Loss Models:** Includes a **Gilbert-Elliott** model to simulate bursty packet losses (useful for wireless scenarios).
    * **Queue Management:** Implements **CoDel (Controlled Delay)** Active Queue Management (AQM) to mitigate bufferbloat.
* **Visualization:** Generates plots for Throughput (Mbps), RTT (ms), and Jain's Fairness Index over time.

## Scenarios

The notebook includes pre-configured experiments to observe behavior under specific conditions:
1.  **Baseline:** Ideal conditions with a clean, stable link.
2.  **Fairness:** Multiple flows competing for bandwidth (e.g., Reno vs. BBR).
3.  **Wireless-like:** Simulation of variable packet loss using the Gilbert-Elliott model.
4.  **Bufferbloat:** Performance analysis with large FIFO queues vs. CoDel AQM.

## Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```

2.  **Install dependencies:**
    It is recommended to use a virtual environment.
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the Notebook:**
    Launch Jupyter Notebook to view and execute the simulation.
    ```bash
    jupyter notebook "I025_I039_I040_CN_Project 3.ipynb"
    ```

## Requirements

* Python 3.x
* numpy
* pandas
* matplotlib
* prettytable
* jupyter

## Structure

* `I025_I039_I040_CN_Project 3.ipynb`: The main simulation code, including classes for `Flow`, `Link`, `Receiver`, and the event loop.
* `requirements.txt`: List of Python dependencies.

## License

[Choose a license, e.g., MIT License]
