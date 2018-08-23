# Sar-Report-To-Png

## Introduction to the script

The function of this bash script is to display a certain field of a `sar` report based on user input.

The user specifies which `sar` report they wish to extract information from, and then the user specifies which field they wish to see.

## Prerequisites

### The sar Library

The `sar` library is a system activity report tool that will be used to collect necessary data. You can get `sar` by typing the following in your terminal:

```bash
$ apt-get install sysstat
```
Unfortunately on some Linux Distributions, there are a couple of configurations that need to be set.

A good tutorial that can be used to make sure that `sar` will create a daily report can be found [here](https://www.crybit.com/sysstat-sar-on-ubuntu-debian/).

### The gnuplot Library

Gnuplot is a graphing tool that will be used to visualize all of the collected data. You can download `gnuplot` from [here](https://sourceforge.net/projects/gnuplot/files/gnuplot/).

### Operating system

This software is built for Linux Distributions such as Ubuntu and LUbuntu.

## How To Run The script

### Step 1

Open your terminal, and then go to the directory where the script is stored in (usually `Downloads`).

### Step 2

In your terminal, enter the following command:

```bash
sar_report_png
```

### Step 3

You will be met with the following prompts:

```bash
please provide the day of the month that you wish to get a report for (DD) >

please provide the month that you wish to get a report for (MM) >

please provide the year that you wish to get a report for (YYYY) >
```

Each of these prompts will ask you for information on the `sar` report you wish to collect data from.

Enter the day in the format `DD` such as `01` for the first prompt.

Enter the month in the format `MM` such as `12` for the second prompt.

Enter the year in the format `YYYY` such as `2018` for the third prompt.

### Step 4

You will be met with the following prompt:

```bash
fields you can choose from:
1 - usr
2 - nice
3 - sys
4 - iowait
5 - steal
6 - irq
7 - soft
8 - guest
9 - gnice
10 - idle

please provide what field you wish to see (number) >
```

Enter the field you wish to see plotted over time. For example, if you wish to see `idle` plotted over time, then type `10`.

### Step 5

Go to your home directory and find the `gnuplot_plots` directory. Open it, and inside it will contain a png of the customized report.
