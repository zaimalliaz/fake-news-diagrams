const Box = ({ title, top, left, color, width = '160px', height = '50px' }) => (
  <div
    style={{
      position: 'absolute',
      top,
      left,
      width,
      height,
      display: 'flex',
      alignItems: 'center',
      justifyContent: 'center',
      fontSize: '15px',
      textAlign: 'center',
      backgroundColor: color || '#fff',
      border: '2px solid #2c3e50',
      borderRadius: '6px',
      fontWeight: '600',
      color: '#2c3e50',
      zIndex: 10,
      boxShadow: '0 2px 4px rgba(0,0,0,0.1)',
    }}
  >
    {title}
  </div>
);

const ArrowLabel = ({ text, x, y, rotation = 0 }) => (
  <text 
    x={x} 
    y={y} 
    fontSize="11px" 
    fontWeight="500"
    fill="#2c3e50"
    textAnchor="middle"
    dominantBaseline="middle"
    style={{
      backgroundColor: 'white',
      padding: '2px 5px',
      borderRadius: '3px',
      border: '1px solid #eee',
    }}
  >
    {text}
  </text>
);

export default function Diagram() {
  return (
    <div
      style={{
        position: 'relative',
        width: '100%',
        height: '700px',
        backgroundColor: '#f8f9fa',
        fontFamily: "'Georgia', 'Times New Roman', serif",
        padding: '30px',
        overflow: 'hidden',
      }}
    >
      {/* Header */}
      <div style={{ textAlign: 'center', marginBottom: '30px' }}>
        <div style={{ 
          fontSize: '12px', 
          fontWeight: 'bold', 
          color: '#c0392b',
          marginBottom: '5px',
          letterSpacing: '1px'
        }}>
          OFFICIAL: SENSITIVE
        </div>
        <h1 style={{
          fontSize: '22px',
          fontWeight: '600',
          margin: '0 auto',
          maxWidth: '800px',
          lineHeight: '1.4',
          color: '#2c3e50'
        }}>
          Manifestation of Belief and Idea in Thought:<br />
          How Disagreement is Negotiated
        </h1>
      </div>

    
