# sample-code
This contains some sample codes from OpenVX mapping of a light-weight tracking system for Synopsys quad-core IP subsystem.

To keep the algorithm and the codes **confidential**, only random part of the codes are selected for demosntration.
The application contains roughly around 20,000 lines of code.

Some info:
- mapping of embedded tracking application for Synopsys IP subsystem (ARC HS family).
- A light-weight visual tracking system for long-term face tracking.
- OpenVX capturing and mapping of a visual tracker with frame-level execution pipeline.
- Mapping of a deep Convolutional Neural Network (CNN) face detector with trainable filters.

Peak inside:

*vxGraphManager.h* contains a graph that performs the tracking part.

The graph consists of:
- Grayscale node
- Integral image node
- Image pyramid node
- CNN node
- Non-max suppression node
- Context-aware tracking node (Picked as a sample in evss_cntx_track_kernel.cpp)
- Cascade detect node
- Learning Node
