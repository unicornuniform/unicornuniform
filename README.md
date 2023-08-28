### Hi there 👋

Installing SVO (without ROS)
https://github.com/uzh-rpg/rpg_svo/wiki/Installation:-Plain-CMake-(No-ROS)

In Sophus/sophus/so2.cpp
Replace:
  unit_complex_.real() = 1.;
  unit_complex_.imag() = 0.;

With:
  unit_complex_.real(1.);
  unit_complex_.imag(0.);


In fast/src/faster_corner_10_sse.cpp
Insert:
// C++17 removed the register keyword, so we define it to nothing so that
// it doesn't cause errors.
#if __cplusplus >= 201703L
#define register
#endif

When making Sophus:
After running make, run make install

<!--
**unicornuniform/unicornuniform** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
