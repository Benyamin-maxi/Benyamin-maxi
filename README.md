Hi- 👋 Hi, I’m @Benyamin-maxi
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Benyamin-maxi/Benyamin-maxi is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
package main

import (
	"fmt"
	"runtime/debug"

	_ "rsc.io/quote"
)

func main() {
	bi, ok := debug.ReadBuildInfo()
	if !ok {
		panic("couldn't read build info")
	}

	fmt.Printf("%s version %s\n", bi.Path, bi.Main.Version)

	for _, d := range bi.Deps {
		fmt.Printf("\tbuilt with %s version %s\n", d.Path, d.Version)
	}
}
