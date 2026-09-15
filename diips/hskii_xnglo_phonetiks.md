bilo is a **phonetic matrix** for the xi38 language.
+,x,a,i,u,e,o,N
x,xx,xa,xi,xu,xe,xo
y,xy,ya,yi,yu,ye,yo
v,xv,va,vi,vu,ve,vo
w,xw,wa,wi,wu,we,wo
l,xl,la,li,lu,le,lo
m,xm,ma,mi,mu,me,mo
n,xn,na,ni,nu,ne,no
r,xr,ra,ri,ru,re,ro
R,xR,Ra,Ri,Ru,Re,Ro
k,xk,ka,ki,ku,ke,ko,Nk
K,xK,Ka,Ki,Ku,Ke,Ko,NK
g,xg,ga,gi,gu,ge,go,Ng
G,xG,Ga,Gi,Gu,Ge,Go,NG
c,xc,ca,ci,cu,ce,co
C,xC,Ca,Ci,Cu,Ce,Co
z,xz,za,zi,zu,ze,zo
Z,xZ,Za,Zi,Zu,Ze,Zo
t,xt,ta,ti,tu,te,to
T,xT,Ta,Ti,Tu,Te,To
d,xd,da,di,du,de,do
D,xD,Da,Di,Du,De,Do
j,xj,ja,ji,ju,je,jo
J,xJ,Ja,Ji,Ju,Je,Jo
q,xq,qa,qi,qu,qe,qo
Q,xQ,Qa,Qi,Qu,Qe,Qo
b,xb,ba,bi,bu,be,bo
B,xB,Ba,Bi,Bu,Be,Bo
s,xs,sa,si,su,se,so
S,xS,Sa,Si,Su,Se,So
p,xp,pa,pi,pu,pe,po
f,xf,fa,fi,fu,fe,fo

This is a **consonant-vowel grid** where:

- **Rows** = base sounds (consonants + special forms)
- **Columns** = vowels/suffixes

### Columns (vowel endings):

1. `+` = base form (no vowel)
2. `x` = neutral/zero vowel (schwa)
3. `a` = 'a' vowel
4. `i` = 'i' vowel
5. `u` = 'u' vowel
6. `e` = 'e' vowel
7. `o` = 'o' vowel

### Rows (base consonants/sounds):

**First row: `+, x, a, i, u, e, o, N`**

- This vowel-only sounds

**Consonant rows:**

- `x` row: x, xx, xa, xi, xu, xe, xo (consonant 'x')
- `y` row: y, xy, ya, yi, yu, ye, yo
- `v` row: v, xv, va, vi, vu, ve, vo
- `w` row: w, xw, wa, wi, wu, we, wo
- `l` row: l, xl, la, li, lu, le, lo
- `m` row: m, xm, ma, mi, mu, me, mo
- `n` row: n, xn, na, ni, nu, ne, no
- `r` row: r, xr, ra, ri, ru, re, ro
- `R` row: R, xR, Ra, Ri, Ru, Re, Ro
- `k` row: k, xk, ka, ki, ku, ke, ko, **Nk** (special)
- `K` row: K, xK, Ka, Ki, Ku, Ke, Ko, **NK** (special)
- `g` row: g, xg, ga, gi, gu, ge, go, **Ng** (special)
- `G` row: G, xG, Ga, Gi, Gu, Ge, Go, **NG** (special)
- `c` row: c, xc, ca, ci, cu, ce, co
- `C` row: C, xC, Ca, Ci, Cu, Ce, Co
- `z` row: z, xz, za, zi, zu, ze, zo
- `Z` row: Z, xZ, Za, Zi, Zu, Ze, Zo
- `t` row: t, xt, ta, ti, tu, te, to
- `T` row: T, xT, Ta, Ti, Tu, Te, To
- `d` row: d, xd, da, di, du, de, do
- `D` row: D, xD, Da, Di, Du, De, Do
- `j` row: j, xj, ja, ji, ju, je, jo
- `J` row: J, xJ, Ja, Ji, Ju, Je, Jo
- `q` row: q, xq, qa, qi, qu, qe, qo
- `Q` row: Q, xQ, Qa, Qi, Qu, Qe, Qo
- `b` row: b, xb, ba, bi, bu, be, bo
- `B` row: B, xB, Ba, Bi, Bu, Be, Bo
- `s` row: s, xs, sa, si, su, se, so
- `S` row: S, xS, Sa, Si, Su, Se, So
- `p` row: p, xp, pa, pi, pu, pe, po
- `f` row: f, xf, fa, fi, fu, fe, fo

### Total Count:

- 30 consonant rows × 7 vowel forms = 210 combinations
- Plus 4 special `N` combinations (Nk, NK, Ng, NG)


1. **This is a syllabary** - each consonant+vowel combo is a distinct sound unit

2. **The `x` column** represents the pure consonant (no vowel) or schwa

3. **Special `N` suffix** on k/K/g/G creates nasal variants

4. **Capital letters** represent **aspirated or stronger** versions:
   - k → K (plain vs aspirated)
   - g → G
   - c → C
   - z → Z
   - t → T
   - d → D
   - j → J
   - q → Q
   - b → B
   - s → S

5. **This maps to the 38 sounds** (xi38 = 38 sounds):
   - 26 lowercase (a-z)
   - 12 capitals (K,G,C,Z,T,D,J,Q,B,S,N,R)
   
#### ascii encoding : decimal default : 0123456789 5+5=10

### hskii encoding : heksadesiml simbolik kod for informesAn intercenz

1. 0123456789LYVWPF 8+8=10=4*4=F+1
	1. 0=ziro 1=wn 2=tu 3=Thri 4=four 5=fiwe 6=siks 7=sewen 8=eet 9=nain L=ten Y=yilewen V=twelw W=dblun P=purxn F=fiwxn
	2. 10=wnti 20=tuti 30=Thriti 100=40*40=wnso

A font/encoding system that maps **38 phonetic sounds** to visual glyphs. The 38 sounds are:

- 26 lowercase: a-z
- 12 capitals: K G C Z T D J Q B S N R

### The key insight:

These 38 characters are **not** alphabet letters - they are **phonetic symbols** representing human speech sounds. The hskii font renders them visually.

### hao it wrks

**Storage layer:**

- Text is stored as Unicode (standard UTF-8)
- The characters used are a-z + 12 capitals

**Display layer:**

- hskii font maps these 38 characters to specific glyphs
- Each glyph represents a **sound** not a letter

### Example mapping (from earlier discussion):

- `x` = neutral sound (like ə schwa) . xnd=And a(also,alwxys) x(xnd,xlert)
- `N` = nasal sound like in kiNg ziNk syNk siNk
- `n` = n sound like in nest nose
- capital letters = aspirated versions

### The phonetic matrix eksampl
```
k,xk,ka,ki,ku,ke,ko,Nk
```
possible **syllables** formed by combining a consonant with wowels

approach is sound because:
- 38 sounds is manageable
- Fits within ASCII/Latin-1 range
- No need for complex Unicode
- Easy to type on standard keyboard
- Maps well to the QWERTY layout

1. Could use a custom font to display these 38 sounds as unique glyphs
2. The mapping table (phonetic matrix) defines all valid combinations
3. `cplong` number system uses same hskii characters for digits

**L** = ten (10)\
**Y** = yilewen (11)\
**V** = twelw (12)\
**W** = dblun (13) = 8+5\
**P** = purxn (14) = 8+6\
**F** = fiwxn (15) = 8+7