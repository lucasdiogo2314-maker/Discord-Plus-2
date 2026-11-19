import { useEffect, useState } from 'react';

export default function App() {
  const [user, setUser] = useState(null);

  useEffect(() => {
    fetch('/api/auth/status')
      .then(r => r.json())
      .then(data => setUser(data.user))
      .catch(() => {});
  }, []);

  return (
    <main style={{
      background: '#0c0f18',
      color: 'white',
      minHeight: '100vh',
      padding: '30px',
      fontFamily: 'Arial'
    }}>
      <h1>Discord Plus 2</h1>
      <p>Seu espaço. Suas comunidades.</p>

      {user ? (
        <h2>Olá, {user.username}!</h2>
      ) : (
        <button onClick={() => {
          window.location.href = '/api/auth/discord';
        }}>
          Conectar conta Discord
        </button>
      )}

      <h2>Seu painel</h2>
      <p>🎮 Jogos</p>
      <p>📞 Chamadas</p>
      <p>📡 Transmissões</p>
      <p>👥 Comunidade</p>
    </main>
  );
}
