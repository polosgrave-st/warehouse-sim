# Warehouse Flow Simulator

An interactive simulation of a four-station warehouse line (receiving, picking, packing, shipping). Change how many orders arrive, how many workers each station has, and how long each order takes, then watch where the line backs up.

**Live demo:** https://polosgrave-st.github.io/warehouse-sim

## What it shows
- Orders arriving at random (Poisson arrivals) and waiting in line at each station
- Worker utilization per station, with the bottleneck highlighted on the floor
- Throughput (orders shipped per hour), cycle time, and work-in-progress
- A live chart of queue lengths at every station
- A Little's Law check (WIP ≈ throughput × cycle time) when the line is stable
- Scenarios: a balanced line, a packing bottleneck, and rush hour

## How it works
Each station can handle `workers × 60 ÷ minutes per order` orders per hour. If orders arrive faster than the slowest station can handle, that station becomes the bottleneck and its queue grows without limit. Work-time variability shows how even a station under capacity can build long lines when it runs near its limit.

Built with plain HTML, CSS, and JavaScript (canvas). No libraries, one file.

By Yousif Abdelbagi, Texas A&M University
