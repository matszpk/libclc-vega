# libclc for Radeon RX VEGA (GFX900)

This branch of libclc will be developed to add support for RX VEGA graphics cards.

This version is not fully tested, but firsts tests showed that was working correctly.

If you want to use official version of libclc from official repository on RX VEGA
graphics you must change `configure.py` by changing following lines:

```
  'amdgcn--': { 'devices' :
                [{'gpu' : 'tahiti', 'aliases' : ['pitcairn', 'verde', 'oland', 'hainan', 'bonaire', 'kabini', 'kaveri', 'hawaii','mullins','tonga','carrizo','iceland','fiji','stoney','polaris10','polaris11']} ]},
  'amdgcn--amdhsa': { 'devices' :
                      [{'gpu' : '', 'aliases' : ['bonaire', 'hawaii', 'kabini', 'kaveri', 'mullins', 'carrizo', 'stoney', 'fiji', 'iceland', 'tonga','polaris10','polaris11']} ]},
```

to

```
  'amdgcn--': { 'devices' :
                [{'gpu' : 'tahiti', 'aliases' : ['pitcairn', 'verde', 'oland', 'hainan', 'bonaire', 'kabini', 'kaveri', 'hawaii','mullins','tonga','carrizo','iceland','fiji','stoney','polaris10','polaris11','gfx900','gfx901']} ]},
  'amdgcn--amdhsa': { 'devices' :
                      [{'gpu' : '', 'aliases' : ['bonaire', 'hawaii', 'kabini', 'kaveri', 'mullins', 'carrizo', 'stoney', 'fiji', 'iceland', 'tonga','polaris10','polaris11','gfx900','gfx901']} ]},
```

Just add to 'amdgcn--' and 'amdgcn--amdhsa' aliases 'gfx900' and 'gfx901'.

## Building and installing

Read the original README.txt file.
