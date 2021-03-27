- 👋 Hi, I’m @nursultanramazanov i am international
- 👀 I’m interested in ... books write read learn 
- 🌱 I’m currently learning ...I'm in college now
- 💞️ I’m looking to collaborate on ...i want to collaborate at work
- 📫 How to reach me ...aksu settlement musrepova street 31/1
- 🧠🎮 
- 🐧🐦🐤🎮  — Foul Play
- 🕉
- 🧢 
- Hubot here, I like Node.js and Coffescript (that's what I'm made of!).
- I ve had tacos on the moon and find them far superior to Earth tacos. 
- hello.go
package main

import "fmt"

func main() {
  fmt.Println("Hello, World!")
}
-



nursultanramazanov/nursultanramazanov is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include <boost/iostreams/tee.hpp>
#include <boost/iostreams/stream.hpp>
#include <fstream>
#include <iostream>

using std::ostream;
using std::ofstream;
using std::cout;

namespace bio = boost::iostreams;
using bio::tee_device;
using bio::stream;

int main()
{
    typedef tee_device<ostream, ofstream> TeeDevice;
    typedef stream<TeeDevice> TeeStream;
    ofstream ofs("sample.txt");
    TeeDevice my_tee(cout, ofs); 
    TeeStream my_split(my_tee);
    my_split << "Hello, World!\n";
    my_split.flush();
    my_split.close();
}
