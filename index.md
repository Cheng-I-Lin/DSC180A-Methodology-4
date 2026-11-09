# DSC 180A Methodology Assignment 4

## Student Information

**Name:** Cheng-I Lin

**UCSD Email:** chl236@ucsd.edu

**Section:** Physical Intelligence for Intelligent Manufacturing (D17)

**Mentor:** Tauhidur Rahman

---

## Quarter 2 Project Brainstorming

**1. What is the most interesting topic covered in your domain this quarter?**

Personally, I think the most interesting topic this quarter was trying out the drone simulations on Isaac Sim and MuJoCo. I haven't done any 3D modeling or simulation before, which is why being able to conduct experiments on a physics based engine simulation platform was intriguing to me. Specifically, I found it interesting how we can simulate adverse environmental conditions and their impact on autonomous drone flights. In MuJoCo, I was able to simulate various wind conditions to test how winds of different magnitude, duration, and direction can affect the drone's PID trajectory tracking. Moreover, I incorporated sensors such as RGB/depth cameras, accelerometer, and gyroscope, capturing the critical data details of how the drone is responding to these wind conditions. This is particularly interesting to me because I found it extremely useful and efficient how one can simply create virtual simulations to mimic real life complex machinery systems and functionalities, reducing the need for certain resources and ensuring a safer, more controlled testing environment.


**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

A potential investigation for the Quarter 2 Project I have in mind is to check whether machine learning models can accurately predict drone instability or potential flight failure before it occurs, using multivariate time series data collected from the simulated drone flights. During the Quarter 1 Project, our group mainly focused on observing the impacts of environmental disturbances and how reinforcement learning algorithms can better control the flights. However, during my simulations on MuJoCo, I noticed that if the wind conditions were too strong or too long (longer duration) then the drone may experience certain motor failures, causing the drone to crash or deviate far away from the intended flight path. Therefore, I want to further investigate if machine learning models can foresee drone failures and reliably generalize results to multiple environmental conditions, allowing the drone to retreat or signal certain warnings before more consequences happen. To accomplish this, I would use simulation generated flight data to identify patterns associated with unstable behavior under different environmental disturbances. By collecting information such as position, velocity, orientation, angular velocity, and control inputs, I could train predictive models to estimate the likelihood of a drone losing stability within a specified time horizon. Lastly, I would then evaluate how accurately and how early these models can identify dangerous flight conditions, particularly when exposed to wind patterns, or other adverse conditions, not encountered during training.


**3. What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

One potential change I would like to make is to transition from exploratory simulation development and controller testing toward a more systematic, hypothesis driven experimental framework. During Quarter 1, most of my work has been dedicated to understanding how the simulation platform of MuJoCo works, how to create certain environmental conditions, and how different flight control algorithms can be implemented. This exploratory process has been necessary because autonomous drone simulation involves several interconnected technical challenges, including modeling flight dynamics, configuring sensors, tuning controllers, and introducing realistic environmental disturbances. However, one limitation of this approach is that experiments can become focused on determining whether a particular simulation or controller functions correctly rather than systematically investigating why certain behaviors occur or how reliably those behaviors can be reproduced. Therefore, I would like to place greater emphasis on establishing controlled experimental conditions and defining measurable performance criteria before conducting large scale simulations for Quarter 2. This can help me develop a more rigorous understanding of the relationship between environmental disturbances, sensor behavior, and drone instability, which is more suitable for the purpose of the Quarter 2 Project and its deliverables.


**4. What other techniques would you be interested in using in your project?**

I would be particularly interested in exploring supervised machine learning, multivariate time series analysis, feature engineering, and model interpretability to better understand and predict drone instability for Quarter 2 Project investigations. Since drone flight produces continuous streams of measurements from sensors and control systems, I believe that analyzing the relationships between these signals could reveal patterns that are difficult to identify through individual measurements alone. One approach I would like to investigate is using traditional classification algorithms, including logistic regression, random forests, and gradient-boosted decision trees, to predict whether a drone will experience an instability event within a predefined future time window. These models would provide useful baselines for evaluating whether more complex approaches offer meaningful improvements. Beyond these traditional supervised learning, I would also be interested in applying temporal modeling techniques that explicitly account for the sequential nature of flight telemetry. For example, Long Short Term Memory (LSTM) networks or Gated Recurrent Units (GRUs) could potentially identify patterns involving changes in orientation, velocity, and acceleration over time. Rather than predicting instability from a single observation, these models could analyze a sequence of recent measurements to determine whether the drone is gradually losing stability. I would compare these temporal models against simpler approaches that use statistical features extracted from sliding windows, such as moving averages, standard deviations, rates of change, and maximum deviations. This comparison would help determine whether the additional complexity of deep learning is justified by improved predictive performance, which serves as a great evaluation technique so that we can know if our project can be seen as an useful product for real world industries.
