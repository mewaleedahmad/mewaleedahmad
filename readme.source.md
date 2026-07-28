```aura width=860 height=180
<div style={{
  width: '100%', height: '100%', background: '#11111b',
  display: 'flex', flexDirection: 'column', justifyContent: 'center',
  fontFamily: 'Inter', position: 'relative', overflow: 'hidden',
  borderRadius: 16, border: '1px solid rgba(180,190,254,0.18)',
  padding: '0 44px',
}}>

  <style>
    {`
      @keyframes drift {
        0% { transform: translate(0px, 0px); }
        50% { transform: translate(50px, -25px); }
        100% { transform: translate(0px, 0px); }
      }
      @keyframes scan {
        0% { transform: translateX(-260px); opacity: 0; }
        12% { opacity: 1; }
        88% { opacity: 1; }
        100% { transform: translateX(860px); opacity: 0; }
      }
      #orb-1 { animation: drift 11s ease-in-out infinite; }
      #scan-1 { animation: scan 6s linear infinite; }
    `}
  </style>

  <svg width="860" height="180" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <pattern id="grid-1" width="26" height="26" patternUnits="userSpaceOnUse">
        <circle cx="1" cy="1" r="1" fill="rgba(205,214,244,0.06)" />
      </pattern>
      <radialGradient id="orbGrad-1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(180,190,254,0.32)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </radialGradient>
      <linearGradient id="scanGrad-1" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(180,190,254,0)" />
        <stop offset="50%" stopColor="rgba(180,190,254,0.85)" />
        <stop offset="100%" stopColor="rgba(180,190,254,0)" />
      </linearGradient>
    </defs>
    <rect width="860" height="180" fill="url(#grid-1)" />
    <ellipse id="orb-1" cx="720" cy="40" rx="220" ry="160" fill="url(#orbGrad-1)" />
    <rect id="scan-1" x="0" y="0" width="260" height="2" fill="url(#scanGrad-1)" />
  </svg>

  <div style={{ display: 'flex', flexDirection: 'column', gap: 8, zIndex: 10 }}>
    <div style={{ display: 'flex', fontSize: 38, fontWeight: 800, color: '#cdd6f4', letterSpacing: '-1px', lineHeight: 1 }}>
      {'Waleed Ahmad'}
    </div>
    <div style={{ display: 'flex', fontSize: 18, color: 'rgba(180,190,254,0.85)', fontWeight: 400, letterSpacing: '0.3px' }}>
      {'Full-Stack Engineer · Linux Enthusiast'}
    </div>
  </div>
</div>
```

```aura width=860 height=290
<div style={{
  width: '100%', height: '100%', background: '#11111b',
  display: 'flex', flexDirection: 'column',
  fontFamily: 'Inter', padding: '26px 40px', gap: 18,
  position: 'relative', overflow: 'hidden',
  borderRadius: 16, border: '1px solid rgba(180,190,254,0.18)',
}}>

  <style>
    {`
      @keyframes drift {
        0% { transform: translate(0px, 0px); }
        50% { transform: translate(-45px, 20px); }
        100% { transform: translate(0px, 0px); }
      }
      @keyframes scan {
        0% { transform: translateX(-260px); opacity: 0; }
        12% { opacity: 1; }
        88% { opacity: 1; }
        100% { transform: translateX(860px); opacity: 0; }
      }
      #orb-2 { animation: drift 13s ease-in-out infinite; }
      #scan-2 { animation: scan 7s linear infinite; }
    `}
  </style>

  <svg width="860" height="290" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <pattern id="grid-2" width="26" height="26" patternUnits="userSpaceOnUse">
        <circle cx="1" cy="1" r="1" fill="rgba(205,214,244,0.06)" />
      </pattern>
      <radialGradient id="orbGrad-2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(203,166,247,0.28)" />
        <stop offset="100%" stopColor="rgba(203,166,247,0)" />
      </radialGradient>
      <linearGradient id="scanGrad-2" x1="0%" y1="0%" x2="100%" y2="0%">
        <stop offset="0%" stopColor="rgba(203,166,247,0)" />
        <stop offset="50%" stopColor="rgba(203,166,247,0.85)" />
        <stop offset="100%" stopColor="rgba(203,166,247,0)" />
      </linearGradient>
    </defs>
    <rect width="860" height="290" fill="url(#grid-2)" />
    <ellipse id="orb-2" cx="130" cy="260" rx="230" ry="160" fill="url(#orbGrad-2)" />
    <rect id="scan-2" x="0" y="0" width="260" height="2" fill="url(#scanGrad-2)" />
  </svg>

  <div style={{ display: 'flex', fontSize: 11, fontWeight: 700, color: 'rgba(180,190,254,0.55)', letterSpacing: '3px', zIndex: 10 }}>
    TECH STACK
  </div>

  <div style={{ display: 'flex', flexDirection: 'column', gap: 18, zIndex: 10 }}>
    {[
      { title: 'Languages', color: '#b4befe', items: ['JavaScript', 'TypeScript', 'PHP', "Lua"] },
      { title: 'Frameworks', color: '#cba6f7', items: ['React.js', 'Next.js', 'Laravel'] },
      { title: 'Databases', color: '#74c7ec', items: ['MongoDB', 'PostgreSQL', 'MySQL'] },
      { title: 'Tools', color: '#f5c2e7', items: ['Prisma', 'Docker', 'Git', 'Linux'] },
    ].map(function(cat) {
      return (
        <div key={cat.title} style={{ display: 'flex', alignItems: 'center', gap: 18 }}>
          <div style={{ display: 'flex', fontSize: 12, fontWeight: 700, color: cat.color, letterSpacing: '1px', width: 100 }}>
            {cat.title.toUpperCase()}
          </div>
          <div style={{ display: 'flex', flexWrap: 'wrap', gap: 9 }}>
            {cat.items.map(function(item) {
              return (
                <div key={item} style={{
                  display: 'flex', padding: '7px 18px', borderRadius: 20,
                  background: 'rgba(205,214,244,0.06)', border: '1px solid rgba(205,214,244,0.16)',
                  color: '#cdd6f4', fontSize: 13, fontWeight: 600,
                }}>{item}</div>
              );
            })}
          </div>
        </div>
      );
    })}
  </div>
</div>
```

```

```
