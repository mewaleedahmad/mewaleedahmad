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
        50% { transform: translate(60px, -25px) scale(1.15); }
        100% { transform: translate(0px, 0px) scale(1); }
      }
      @keyframes floatOrb2 {
        0% { transform: translate(0px, 0px) scale(1); }
        50% { transform: translate(-50px, 30px) scale(1.2); }
        100% { transform: translate(0px, 0px) scale(1); }
      }
      @keyframes scanline {
        0% { transform: translateX(-300px); opacity: 0; }
        20% { opacity: 0.95; }
        80% { opacity: 0.95; }
        100% { transform: translateX(860px); opacity: 0; }
      }
      #orb-1 { animation: floatOrb1 11s ease-in-out infinite; }
      #orb-2 { animation: floatOrb2 15s ease-in-out infinite; }
      #scan-1 { animation: scanline 6s ease-in-out infinite; }
    `}
  </style>

  <svg width="860" height="180" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="orbGrad-1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(180,190,254,0.42)" />
        <stop offset="60%" stopColor="rgba(180,190,254,0.12)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </radialGradient>
      <radialGradient id="orbGrad-2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(203,166,247,0.36)" />
        <stop offset="70%" stopColor="rgba(203,166,247,0.08)" />
        <stop offset="100%" stopColor="rgba(203,166,247,0)" />
      </radialGradient>
      <linearGradient id="scanGrad-1" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(180,190,254,0)" />
        <stop offset="50%" stopColor="rgba(180,190,254,1)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </linearGradient>
    </defs>
    <ellipse id="orb-1" cx="740" cy="30" rx="250" ry="170" fill="url(#orbGrad-1)" />
    <ellipse id="orb-2" cx="120" cy="150" rx="210" ry="140" fill="url(#orbGrad-2)" />
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

```aura width=860 height=350
<div style={{
  width: '100%', height: '100%', background: '#11111b',
  display: 'flex', flexDirection: 'column',
  fontFamily: 'Inter', padding: '28px 40px', gap: 14,
  position: 'relative', overflow: 'hidden',
  borderRadius: 16, border: '1px solid rgba(180,190,254,0.24)',
}}>

  <style>
    {`
      @keyframes floatOrbStack {
        0% { transform: translate(0px, 0px) scale(1); }
        50% { transform: translate(-50px, 30px) scale(1.15); }
        100% { transform: translate(0px, 0px) scale(1); }
      }
      @keyframes scanlineStack {
        0% { transform: translateX(-300px); opacity: 0; }
        20% { opacity: 0.95; }
        80% { opacity: 0.95; }
        100% { transform: translateX(860px); opacity: 0; }
      }
      #orb-stack { animation: floatOrbStack 13s ease-in-out infinite; }
      #scan-stack { animation: scanlineStack 7s ease-in-out infinite; }
    `}
  </style>

  <svg width="860" height="350" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="orbGradStack" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(180,190,254,0.36)" />
        <stop offset="60%" stopColor="rgba(203,166,247,0.14)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </radialGradient>
      <linearGradient id="scanGradStack" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(180,190,254,0)" />
        <stop offset="50%" stopColor="rgba(180,190,254,0.95)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </linearGradient>
    </defs>
    <ellipse id="orb-stack" cx="150" cy="300" rx="270" ry="190" fill="url(#orbGradStack)" />
    <rect id="scan-stack" x="0" y="0" width="300" height="2" fill="url(#scanGradStack)" />
  </svg>

  <div style={{ display: 'flex', alignItems: 'center', gap: 10, marginBottom: 12 }}>
    <div style={{ width: 4, height: 16, borderRadius: 2, background: '#b4befe' }} />
    <div style={{ display: 'flex', fontSize: 12, fontWeight: 800, color: '#b4befe', letterSpacing: '3px' }}>
      TECH STACK
    </div>
  </div>

  <div style={{ display: 'flex', flexDirection: 'column', gap: 16 }}>
    {[
      { title: 'Languages', color: '#b4befe', items: ['JavaScript', 'TypeScript', 'PHP', 'Lua'] },
      { title: 'Frameworks', color: '#cba6f7', items: ['React.js', 'Next.js', 'Laravel'] },
      { title: 'Databases & ORM', color: '#74c7ec', items: ['MongoDB', 'PostgreSQL', 'MySQL', 'Prisma'] },
      { title: 'DevOps', color: '#f5c2e7', items: ['Docker', 'Git', 'Cloudflare'] },
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

```aura width=860 height=195
<div style={{
  width: '100%', height: '100%', background: '#11111b',
  display: 'flex', flexDirection: 'column',
  fontFamily: 'Inter', padding: '26px 40px', gap: 14,
  position: 'relative', overflow: 'hidden',
  borderRadius: 16, border: '1px solid rgba(180,190,254,0.24)',
}}>

  <style>
    {`
      @keyframes floatOrbSys {
        0% { transform: translate(0px, 0px) scale(1); }
        50% { transform: translate(45px, -20px) scale(1.15); }
        100% { transform: translate(0px, 0px) scale(1); }
      }
      @keyframes scanlineSys {
        0% { transform: translateX(-300px); opacity: 0; }
        20% { opacity: 0.95; }
        80% { opacity: 0.95; }
        100% { transform: translateX(860px); opacity: 0; }
      }
      #orb-sys { animation: floatOrbSys 11s ease-in-out infinite; }
      #scan-sys { animation: scanlineSys 6.5s ease-in-out infinite; }
    `}
  </style>

  <svg width="860" height="195" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="orbGradSys" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(180,190,254,0.36)" />
        <stop offset="60%" stopColor="rgba(148,226,213,0.14)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </radialGradient>
      <linearGradient id="scanGradSys" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(180,190,254,0)" />
        <stop offset="50%" stopColor="rgba(180,190,254,0.95)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </linearGradient>
    </defs>
    <ellipse id="orb-sys" cx="720" cy="140" rx="250" ry="170" fill="url(#orbGradSys)" />
    <rect id="scan-sys" x="0" y="0" width="300" height="2" fill="url(#scanGradSys)" />
  </svg>

  <div style={{ display: 'flex', alignItems: 'center', gap: 10, marginBottom: 12 }}>
    <div style={{ width: 4, height: 16, borderRadius: 2, background: '#b4befe' }} />
    <div style={{ display: 'flex', fontSize: 12, fontWeight: 800, color: '#b4befe', letterSpacing: '3px' }}>
      SYSTEM & DEV ENVIRONMENT
    </div>
  </div>

  <div style={{ display: 'flex', gap: 16 }}>
    {[
      { label: 'OS', value: 'Arch Linux', color: '#74c7ec' },
      { label: 'WM', value: 'Niri', color: '#b4befe' },
      { label: 'TERMINAL', value: 'WezTerm', color: '#94e2d5' },
      { label: 'EDITOR', value: 'Neovim', color: '#a6e3a1' },
    ].map(function(item) {
      return (
        <div key={item.label} style={{
          flex: 1, display: 'flex', flexDirection: 'column', gap: 6,
          padding: '18px 20px', borderRadius: 14,
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
