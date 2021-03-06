What are palettes
-----------------

Color palettes are used in 8 bit indexed images and can have up to 256
colors. It's called indexing because a palette is a list with r,g,b
values denoted with an index number (wich is the color value). This is a
cornerstone of functions like
[Map\_get\_pixel](Map_get_pixel "wikilink")().

More information: [Indexed
color](http://en.wikipedia.org/wiki/Indexed_color), [Color look-up
tables](http://en.wikipedia.org/wiki/CLUT)

The system palette
------------------

    uint8_t default_palette[] =
        {
        0, 0, 0, /* Color 0 */
        16, 16, 16, /* Color 1 */
        32, 32, 32, /* Color 2 */
        48, 48, 48, /* Color 3 */
        64, 64, 64, /* Color 4 */
        84, 84, 84, /* Color 5 */
        100, 100, 100, /* Color 6 */
        116, 116, 116, /* Color 7 */
        132, 132, 132, /* Color 8 */
        148, 148, 148, /* Color 9 */
        168, 168, 168, /* Color 10 */
        184, 184, 184, /* Color 11 */
        200, 200, 200, /* Color 12 */
        216, 216, 216, /* Color 13 */
        232, 232, 232, /* Color 14 */
        252, 252, 252, /* Color 15 */
        40, 0, 0, /* Color 16 */
        72, 0, 0, /* Color 17 */
        108, 0, 0, /* Color 18 */
        144, 0, 0, /* Color 19 */
        180, 0, 0, /* Color 20 */
        216, 0, 0, /* Color 21 */
        252, 0, 0, /* Color 22 */
        252, 32, 0, /* Color 23 */
        252, 64, 0, /* Color 24 */
        252, 96, 0, /* Color 25 */
        252, 128, 0, /* Color 26 */
        252, 160, 0, /* Color 27 */
        252, 180, 56, /* Color 28 */
        252, 200, 112, /* Color 29 */
        252, 220, 168, /* Color 30 */
        252, 240, 224, /* Color 31 */
        0, 40, 0, /* Color 32 */
        0, 60, 0, /* Color 33 */
        0, 84, 0, /* Color 34 */
        0, 108, 0, /* Color 35 */
        0, 132, 0, /* Color 36 */
        0, 156, 0, /* Color 37 */
        0, 180, 0, /* Color 38 */
        0, 204, 0, /* Color 39 */
        0, 228, 0, /* Color 40 */
        0, 252, 0, /* Color 41 */
        48, 252, 32, /* Color 42 */
        96, 252, 64, /* Color 43 */
        144, 252, 96, /* Color 44 */
        192, 252, 132, /* Color 45 */
        216, 252, 176, /* Color 46 */
        240, 252, 220, /* Color 47 */
        0, 0, 40, /* Color 48 */
        0, 0, 72, /* Color 49 */
        0, 0, 104, /* Color 50 */
        0, 0, 140, /* Color 51 */
        0, 0, 172, /* Color 52 */
        0, 0, 208, /* Color 53 */
        0, 0, 252, /* Color 54 */
        0, 48, 252, /* Color 55 */
        0, 100, 252, /* Color 56 */
        0, 148, 252, /* Color 57 */
        0, 200, 252, /* Color 58 */
        0, 252, 252, /* Color 59 */
        56, 252, 252, /* Color 60 */
        112, 252, 252, /* Color 61 */
        168, 252, 252, /* Color 62 */
        224, 252, 252, /* Color 63 */
        28, 28, 0, /* Color 64 */
        52, 52, 0, /* Color 65 */
        76, 76, 0, /* Color 66 */
        100, 100, 0, /* Color 67 */
        124, 124, 0, /* Color 68 */
        152, 152, 0, /* Color 69 */
        176, 176, 0, /* Color 70 */
        200, 200, 0, /* Color 71 */
        224, 224, 0, /* Color 72 */
        252, 252, 0, /* Color 73 */
        252, 252, 36, /* Color 74 */
        252, 252, 72, /* Color 75 */
        252, 252, 108, /* Color 76 */
        252, 252, 144, /* Color 77 */
        252, 252, 180, /* Color 78 */
        252, 252, 220, /* Color 79 */
        28, 0, 28, /* Color 80 */
        52, 0, 52, /* Color 81 */
        76, 0, 76, /* Color 82 */
        100, 0, 100, /* Color 83 */
        124, 0, 124, /* Color 84 */
        152, 0, 152, /* Color 85 */
        176, 0, 176, /* Color 86 */
        200, 0, 200, /* Color 87 */
        224, 0, 224, /* Color 88 */
        252, 0, 252, /* Color 89 */
        252, 36, 252, /* Color 90 */
        252, 72, 252, /* Color 91 */
        252, 112, 252, /* Color 92 */
        252, 148, 252, /* Color 93 */
        252, 184, 252, /* Color 94 */
        252, 224, 252, /* Color 95 */
        0, 20, 20, /* Color 96 */
        0, 40, 40, /* Color 97 */
        0, 60, 60, /* Color 98 */
        0, 80, 80, /* Color 99 */
        0, 104, 100, /* Color 100 */
        0, 124, 120, /* Color 101 */
        0, 144, 144, /* Color 102 */
        0, 164, 164, /* Color 103 */
        0, 188, 184, /* Color 104 */
        0, 208, 204, /* Color 105 */
        0, 228, 224, /* Color 106 */
        0, 252, 248, /* Color 107 */
        44, 252, 248, /* Color 108 */
        92, 252, 248, /* Color 109 */
        140, 252, 248, /* Color 110 */
        188, 252, 248, /* Color 111 */
        24, 12, 0, /* Color 112 */
        44, 24, 0, /* Color 113 */
        64, 36, 0, /* Color 114 */
        84, 48, 0, /* Color 115 */
        108, 60, 0, /* Color 116 */
        128, 72, 0, /* Color 117 */
        148, 84, 0, /* Color 118 */
        168, 96, 0, /* Color 119 */
        192, 112, 0, /* Color 120 */
        196, 128, 28, /* Color 121 */
        204, 144, 60, /* Color 122 */
        212, 160, 92, /* Color 123 */
        216, 180, 120, /* Color 124 */
        224, 196, 152, /* Color 125 */
        232, 212, 184, /* Color 126 */
        240, 232, 216, /* Color 127 */
        24, 12, 12, /* Color 128 */
        40, 20, 20, /* Color 129 */
        60, 32, 32, /* Color 130 */
        80, 44, 44, /* Color 131 */
        96, 52, 52, /* Color 132 */
        116, 64, 64, /* Color 133 */
        136, 76, 76, /* Color 134 */
        156, 88, 88, /* Color 135 */
        176, 104, 104, /* Color 136 */
        196, 120, 120, /* Color 137 */
        216, 136, 136, /* Color 138 */
        240, 152, 152, /* Color 139 */
        240, 168, 168, /* Color 140 */
        244, 188, 188, /* Color 141 */
        244, 204, 204, /* Color 142 */
        248, 224, 224, /* Color 143 */
        24, 20, 12, /* Color 144 */
        44, 36, 24, /* Color 145 */
        68, 52, 36, /* Color 146 */
        88, 72, 48, /* Color 147 */
        112, 88, 60, /* Color 148 */
        132, 104, 72, /* Color 149 */
        156, 124, 88, /* Color 150 */
        172, 140, 100, /* Color 151 */
        188, 156, 112, /* Color 152 */
        204, 176, 124, /* Color 153 */
        220, 192, 136, /* Color 154 */
        240, 212, 152, /* Color 155 */
        240, 216, 168, /* Color 156 */
        244, 224, 188, /* Color 157 */
        244, 232, 204, /* Color 158 */
        248, 240, 224, /* Color 159 */
        32, 8, 0, /* Color 160 */
        60, 16, 0, /* Color 161 */
        88, 28, 0, /* Color 162 */
        120, 36, 0, /* Color 163 */
        148, 48, 0, /* Color 164 */
        176, 56, 0, /* Color 165 */
        208, 68, 0, /* Color 166 */
        216, 88, 0, /* Color 167 */
        224, 112, 0, /* Color 168 */
        232, 136, 0, /* Color 169 */
        240, 160, 0, /* Color 170 */
        252, 184, 0, /* Color 171 */
        252, 200, 56, /* Color 172 */
        252, 216, 112, /* Color 173 */
        252, 232, 168, /* Color 174 */
        252, 252, 224, /* Color 175 */
        20, 12, 12, /* Color 176 */
        36, 24, 24, /* Color 177 */
        56, 36, 36, /* Color 178 */
        72, 48, 48, /* Color 179 */
        92, 64, 64, /* Color 180 */
        108, 76, 76, /* Color 181 */
        128, 88, 88, /* Color 182 */
        144, 100, 100, /* Color 183 */
        164, 116, 116, /* Color 184 */
        172, 132, 132, /* Color 185 */
        184, 148, 148, /* Color 186 */
        192, 164, 164, /* Color 187 */
        204, 180, 180, /* Color 188 */
        212, 196, 196, /* Color 189 */
        224, 212, 212, /* Color 190 */
        236, 232, 232, /* Color 191 */
        12, 20, 12, /* Color 192 */
        24, 36, 24, /* Color 193 */
        36, 56, 36, /* Color 194 */
        48, 72, 48, /* Color 195 */
        64, 92, 64, /* Color 196 */
        76, 108, 76, /* Color 197 */
        88, 128, 88, /* Color 198 */
        100, 144, 100, /* Color 199 */
        116, 164, 116, /* Color 200 */
        132, 172, 132, /* Color 201 */
        148, 184, 148, /* Color 202 */
        164, 192, 164, /* Color 203 */
        180, 204, 180, /* Color 204 */
        196, 212, 196, /* Color 205 */
        212, 224, 212, /* Color 206 */
        232, 236, 232, /* Color 207 */
        12, 12, 16, /* Color 208 */
        24, 24, 32, /* Color 209 */
        36, 36, 48, /* Color 210 */
        48, 48, 64, /* Color 211 */
        64, 64, 80, /* Color 212 */
        76, 76, 96, /* Color 213 */
        88, 88, 112, /* Color 214 */
        100, 100, 128, /* Color 215 */
        116, 116, 148, /* Color 216 */
        132, 132, 160, /* Color 217 */
        148, 148, 172, /* Color 218 */
        164, 164, 184, /* Color 219 */
        180, 180, 196, /* Color 220 */
        196, 196, 208, /* Color 221 */
        212, 212, 220, /* Color 222 */
        232, 232, 236, /* Color 223 */
        40, 0, 0, /* Color 224 */
        80, 0, 0, /* Color 225 */
        124, 0, 0, /* Color 226 */
        164, 0, 0, /* Color 227 */
        208, 0, 0, /* Color 228 */
        252, 0, 0, /* Color 229 */
        252, 40, 0, /* Color 230 */
        252, 84, 0, /* Color 231 */
        252, 124, 0, /* Color 232 */
        252, 168, 0, /* Color 233 */
        252, 208, 0, /* Color 234 */
        252, 252, 0, /* Color 235 */
        252, 252, 44, /* Color 236 */
        252, 252, 92, /* Color 237 */
        252, 252, 140, /* Color 238 */
        252, 252, 188, /* Color 239 */
        0, 0, 0, /* Color 240 */
        0, 0, 88, /* Color 241 */
        0, 0, 128, /* Color 242 */
        0, 0, 168, /* Color 243 */
        0, 0, 208, /* Color 244 */
        0, 0, 248, /* Color 245 */
        40, 0, 248, /* Color 246 */
        84, 0, 248, /* Color 247 */
        124, 0, 248, /* Color 248 */
        168, 0, 248, /* Color 249 */
        208, 0, 248, /* Color 250 */
        252, 0, 252, /* Color 251 */
        252, 52, 252, /* Color 252 */
        252, 108, 252, /* Color 253 */
        252, 164, 252, /* Color 254 */
        252, 220, 252 /* Color 255 */
        } ;

<Category:palettes> <Category:mod_map>
