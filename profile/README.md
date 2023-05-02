# VnVLabs:

Welcome to VnVLabs.com, where the cloud meets simplicity! With VnVLabs, you can easily provision on-demand resources on AWS using your own AWS account. And that's just the beginning.

Our platform boasts a simple and intuitive interface for provisioning and managing resources, including support for any EC2 instance type. Once you've provisioned a compute resource, simply ask VnVLabs to launch a docker container on that resource, and we'll take it from there.

We'll take your docker container and wrap it up inside our custom docker image, which includes an integrated VSCode-like IDE, an integrated Paraview Visualizer, and an integrated file browser. You can then interact with the IDE, Visualizer, and file browser through our web-based interface. It's that easy!

But we don't stop there. VnVLabs supports any Ubuntu-based docker image, so you can bring your own custom image and get started right away. And for developers who want even more control, we offer the VnVToolkit, a C/C++ API that can be used within C/C++ and FORTRAN applications. With the VnVToolkit, you can control how your software is presented within the VnVLabs GUI and take advantage of a range of verification and validation processes.

Our features include a built-in unit testing framework, function-level integration testing (configurable at runtime by the end-user), application-level integration testing, provenance tracking, input file validation, live data visualization using real simulation data, performance monitoring, uncertainty quantification, and sensitivity analysis.

So why wait? Try VnVLabs today and experience the power of cloud computing with the simplicity you deserve.

Each repository contains its own licensing information. FFor the most part, all vnvlabs code (the core api,
the gui, the SAAS server and a few of the application examples) are released using the three clause BSD license. 

This repository includes a number of forks for third party software. All software forks (moose,libmesh,petsc,hypre,mfem,asgard,
swfft,xs-bench,miniamr,etc.) are simply exist only for demonstration and testing purposes. We will attempt to keep these forks up
to date with the upstream repositories, however, we make no claims that they are up to date at any given time. The hope is that our VnV 
modifications will eventually make their way into the upstream codebases, removing the need for the vnvlabs forks. 
   
   
   
   
