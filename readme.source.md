```aura width=860 height=180
<div style={{
  width: '100%', height: '100%', background: '#11111b',
  display: 'flex', flexDirection: 'column', justifyContent: 'center',
  fontFamily: 'Inter', position: 'relative', overflow: 'hidden',
  borderRadius: 16, border: '1px solid rgba(180,190,254,0.24)',
  padding: '0 44px',
}}>

  <style>
    {`
      @keyframes floatOrb1 {
        0% { transform: translate(0px, 0px) scale(1); }
        50% { transform: translate(45px, -20px) scale(1.1); }
        100% { transform: translate(0px, 0px) scale(1); }
      }
      @keyframes floatOrb2 {
        0% { transform: translate(0px, 0px) scale(1); }
        50% { transform: translate(-45px, 20px) scale(1.1); }
        100% { transform: translate(0px, 0px) scale(1); }
      }
      @keyframes scanline {
        0% { transform: translateX(-300px); opacity: 0; }
        20% { opacity: 0.9; }
        80% { opacity: 0.9; }
        100% { transform: translateX(860px); opacity: 0; }
      }
      #orb-1-1 { animation: floatOrb1 5s ease-in-out infinite; }
      #orb-1-2 { animation: floatOrb2 5s ease-in-out infinite; }
      #scan-1 { animation: scanline 3.5s linear infinite; }
    `}
  </style>

  <svg width="860" height="180" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="orbGrad1-1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(180,190,254,0.45)" />
        <stop offset="60%" stopColor="rgba(137,180,250,0.15)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </radialGradient>
      <radialGradient id="orbGrad1-2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(137,180,250,0.38)" />
        <stop offset="70%" stopColor="rgba(180,190,254,0.1)" />
        <stop offset="100%" stopColor="rgba(137,180,250,0)" />
      </radialGradient>
      <linearGradient id="scanGrad-1" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(180,190,254,0)" />
        <stop offset="50%" stopColor="rgba(180,190,254,0.95)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </linearGradient>
    </defs>
    <ellipse id="orb-1-1" cx="740" cy="30" rx="250" ry="170" fill="url(#orbGrad1-1)" />
    <ellipse id="orb-1-2" cx="120" cy="150" rx="210" ry="140" fill="url(#orbGrad1-2)" />
    <rect id="scan-1" x="0" y="0" width="300" height="2" fill="url(#scanGrad-1)" />
  </svg>

  <div style={{ display: 'flex', flexDirection: 'column', gap: 8 }}>
    <div style={{ display: 'flex', fontSize: 40, fontWeight: 800, color: '#cdd6f4', letterSpacing: '-1px', lineHeight: 1 }}>
      {'Waleed Ahmad'}
    </div>
    <div style={{ display: 'flex', fontSize: 18, color: '#b4befe', fontWeight: 500, letterSpacing: '0.4px' }}>
      {'Full-Stack Engineer · Linux Enthusiast'}
    </div>
  </div>
</div>
```

```aura width=860 height=285
<div style={{
  width: '100%', height: '100%', background: '#11111b',
  display: 'flex', flexDirection: 'column',
  fontFamily: 'Inter', padding: '26px 40px',
  position: 'relative', overflow: 'hidden',
  borderRadius: 16, border: '1px solid rgba(180,190,254,0.24)',
}}>

  <style>
    {`
      @keyframes floatOrb2-1 {
        0% { transform: translate(0px, 0px) scale(1); }
        50% { transform: translate(-45px, -20px) scale(1.1); }
        100% { transform: translate(0px, 0px) scale(1); }
      }
      @keyframes floatOrb2-2 {
        0% { transform: translate(0px, 0px) scale(1); }
        50% { transform: translate(45px, 20px) scale(1.1); }
        100% { transform: translate(0px, 0px) scale(1); }
      }
      @keyframes scanline2 {
        0% { transform: translateX(-300px); opacity: 0; }
        20% { opacity: 0.9; }
        80% { opacity: 0.9; }
        100% { transform: translateX(860px); opacity: 0; }
      }
      #orb-2-1 { animation: floatOrb2-1 5s ease-in-out infinite; }
      #orb-2-2 { animation: floatOrb2-2 5s ease-in-out infinite; }
      #scan-2 { animation: scanline2 3.5s linear infinite; }
    `}
  </style>

  <svg width="860" height="285" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="orbGrad2-1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(180,190,254,0.42)" />
        <stop offset="60%" stopColor="rgba(137,180,250,0.12)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </radialGradient>
      <radialGradient id="orbGrad2-2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(116,199,236,0.38)" />
        <stop offset="70%" stopColor="rgba(180,190,254,0.08)" />
        <stop offset="100%" stopColor="rgba(116,199,236,0)" />
      </radialGradient>
      <linearGradient id="scanGrad-2" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(180,190,254,0)" />
        <stop offset="50%" stopColor="rgba(180,190,254,0.95)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </linearGradient>
    </defs>
    <ellipse id="orb-2-1" cx="720" cy="240" rx="260" ry="170" fill="url(#orbGrad2-1)" />
    <ellipse id="orb-2-2" cx="140" cy="40" rx="220" ry="150" fill="url(#orbGrad2-2)" />
    <rect id="scan-2" x="0" y="0" width="300" height="2" fill="url(#scanGrad-2)" />
  </svg>

  <div style={{ display: 'flex', alignItems: 'center', gap: 10, marginBottom: 20 }}>
    <div style={{ width: 4, height: 16, borderRadius: 2, background: '#b4befe' }} />
    <div style={{ display: 'flex', fontSize: 12, fontWeight: 800, color: '#b4befe', letterSpacing: '3px' }}>
      TECH STACK
    </div>
  </div>

  <div style={{ display: 'flex', flexDirection: 'column', gap: 14 }}>
    {[
      { title: 'Languages', color: '#b4befe', items: ['JavaScript', 'TypeScript', 'PHP'] },
      { title: 'Frameworks', color: '#89b4fa', items: ['React.js', 'Next.js', 'Laravel'] },
      { title: 'Databases & ORM', color: '#74c7ec', items: ['MongoDB', 'PostgreSQL', 'Prisma'] },
      { title: 'DevOps', color: '#89dceb', items: ['Docker', 'Git', 'Cloudflare'] },
    ].map(function(cat) {
      return (
        <div key={cat.title} style={{ display: 'flex', alignItems: 'center', gap: 16 }}>
          <div style={{ display: 'flex', fontSize: 12, fontWeight: 700, color: cat.color, letterSpacing: '1px', width: 160 }}>
            {cat.title.toUpperCase()}
          </div>
          <div style={{ display: 'flex', flexWrap: 'wrap', gap: 10 }}>
            {cat.items.map(function(item) {
              return (
                <div key={item} style={{
                  display: 'flex', padding: '7px 18px', borderRadius: 24,
                  background: 'linear-gradient(135deg, rgba(180,190,254,0.1) 0%, rgba(30,30,46,0.45) 100%)',
                  border: '1px solid rgba(180,190,254,0.25)',
                  color: '#cdd6f4', fontSize: 13, fontWeight: 600, letterSpacing: '0.3px',
                }}>
                  {item}
                </div>
              );
            })}
          </div>
        </div>
      );
    })}
  </div>
</div>
```

```aura width=860 height=165
<div style={{
  width: '100%', height: '100%', background: '#11111b',
  display: 'flex', flexDirection: 'column',
  fontFamily: 'Inter', padding: '24px 40px',
  position: 'relative', overflow: 'hidden',
  borderRadius: 16, border: '1px solid rgba(180,190,254,0.24)',
}}>

  <style>
    {`
      @keyframes floatOrb3-1 {
        0% { transform: translate(0px, 0px) scale(1); }
        50% { transform: translate(-45px, 20px) scale(1.1); }
        100% { transform: translate(0px, 0px) scale(1); }
      }
      @keyframes floatOrb3-2 {
        0% { transform: translate(0px, 0px) scale(1); }
        50% { transform: translate(45px, -20px) scale(1.1); }
        100% { transform: translate(0px, 0px) scale(1); }
      }
      @keyframes scanline3 {
        0% { transform: translateX(-300px); opacity: 0; }
        20% { opacity: 0.9; }
        80% { opacity: 0.9; }
        100% { transform: translateX(860px); opacity: 0; }
      }
      #orb-3-1 { animation: floatOrb3-1 5s ease-in-out infinite; }
      #orb-3-2 { animation: floatOrb3-2 5s ease-in-out infinite; }
      #scan-3 { animation: scanline3 3.5s linear infinite; }
    `}
  </style>

  <svg width="860" height="165" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="orbGrad3-1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(180,190,254,0.42)" />
        <stop offset="60%" stopColor="rgba(137,180,250,0.12)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </radialGradient>
      <radialGradient id="orbGrad3-2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(137,180,250,0.35)" />
        <stop offset="70%" stopColor="rgba(180,190,254,0.08)" />
        <stop offset="100%" stopColor="rgba(137,180,250,0)" />
      </radialGradient>
      <linearGradient id="scanGrad-3" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(180,190,254,0)" />
        <stop offset="50%" stopColor="rgba(180,190,254,0.95)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </linearGradient>
    </defs>
    <ellipse id="orb-3-1" cx="750" cy="90" rx="250" ry="160" fill="url(#orbGrad3-1)" />
    <ellipse id="orb-3-2" cx="220" cy="160" rx="230" ry="140" fill="url(#orbGrad3-2)" />
    <rect id="scan-3" x="0" y="0" width="300" height="2" fill="url(#scanGrad-3)" />
  </svg>

  <div style={{ display: 'flex', alignItems: 'center', gap: 10, marginBottom: 20 }}>
    <div style={{ width: 4, height: 16, borderRadius: 2, background: '#b4befe' }} />
    <div style={{ display: 'flex', fontSize: 12, fontWeight: 800, color: '#b4befe', letterSpacing: '3px' }}>
      DEV ENVIRONMENT
    </div>
  </div>

  <div style={{ display: 'flex', gap: 16 }}>
    {[
      { label: 'OS', value: 'Arch Linux', color: '#74c7ec' },
      { label: 'WM', value: 'Niri', color: '#b4befe' },
      { label: 'TERMINAL', value: 'WezTerm', color: '#89b4fa' },
      { label: 'CODE EDITOR', value: 'Neovim', color: '#89dceb' },
    ].map(function(item) {
      return (
        <div key={item.label} style={{
          flex: 1, display: 'flex', flexDirection: 'column', gap: 6,
          padding: '16px 18px', borderRadius: 14,
          background: 'linear-gradient(135deg, rgba(180,190,254,0.08) 0%, rgba(30,30,46,0.5) 100%)',
          border: '1px solid rgba(180,190,254,0.22)',
        }}>
          <div style={{ fontSize: 11, fontWeight: 700, color: item.color, letterSpacing: '2px' }}>
            {item.label}
          </div>
          <div style={{ fontSize: 16, fontWeight: 700, color: '#cdd6f4', letterSpacing: '0.2px' }}>
            {item.value}
          </div>
        </div>
      );
    })}
  </div>
</div>
```
