Fix kernel panic related to 
  Kernel Extensions in backtrace:
         com.apple.iokit.IOPCIFamily(2.9)[03565C8B-2960-3B32-92FD-E6E86917FE61]@0xffffff801ba03000->0xffffff801ba2efff
         as.vit9696.WhateverGreen(1.5.8)[82AA95B6-925F-35BF-A10E-527D98B3F235]@0xffffff801cf27000->0xffffff801cfa3fff
            dependency: as.vit9696.Lilu(1.6.0)[6167D1C2-7FCA-3319-8246-9CAAFA704235]@0xffffff801ce19000->0xffffff801ce43fff
            dependency: com.apple.iokit.IOPCIFamily(2.9)[03565C8B-2960-3B32-92FD-E6E86917FE61]@0xffffff801ba03000->0xffffff801ba2efff
"Hey, I found the fix for ethernet: set device id to F0000000(wrong id) and add to boot args: dk.e1000=0. Ran for 1h and no kernel panic :D"
https://www.reddit.com/r/hackintosh/comments/qltzxh/10700k_build_monterey_causing_kernel_panics_per/hj5xwca/


