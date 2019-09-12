# Computer Vision

### **Computer Vision**

**"Extract enough information of the world from visual data to make good decisions"**  


**Lambert's Wall**

**- infinitely high wall on an infinite plane with uniform lighting from the infinite sky.**

**- all points will be equally bright \(assuming no interference, no reflection, no radiation, no transmissions\)**  


**Now imagine a point p where the wall stops on one side**

**- no longer uniform**

**- p is now creating a line of maximal brightness away from the wall.**  


**you can apply this to ambient occlusion shading where pixel brightness is equal to the percent of the sky or light source exposed.**  


**light gets absorbed, transmitted, reflected, or get more complicated like fluorescence**  


**BRDF?**

**bidirectional reflectance distribution function**

**- hard to measure, unstable, highly reactive to small changes**  


**You can simplify with "rough" surfaces, the light leaving is independent of exit angle**

**roughness is microfacets scattering light randomly. Meaning reflection is approximately equal in all directions.**

**"diffuse" reflection**

**Lambert's Law**  


**Specular Reflection**

**reflects perfectly, so only in the direction of the source of light \(the angle of incidence is the angle of reflection on the plane of the source vector and reflection vector\)**  


**On real surfaces, energy usually goes in a lobe of direction**  


[**https://en.wikipedia.org/wiki/Photometric\_stereo**](https://en.wikipedia.org/wiki/Photometric_stereo)

[**https://en.wikipedia.org/wiki/Bidirectional\_reflectance\_distribution\_function**](https://en.wikipedia.org/wiki/Bidirectional_reflectance_distribution_function)  


