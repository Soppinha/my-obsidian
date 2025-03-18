Autenticação é o processo de verificar a identidade de um usuário, sistema ou dispositivo para garantir que ele é quem afirma ser. Em termos de tecnologia, é uma etapa crucial para controlar o acesso a sistemas, redes, aplicativos ou dados sensíveis.
![[what_is_authentication_password_example.webp]]
### Principais Formas de Autenticação:

1. **Algo que você sabe**:
    - Utiliza informações conhecidas apenas pelo usuário, como senhas ou PINs.

1. **Algo que você possui**:
    - Baseia-se em um item físico que o usuário tem, como um token, cartão de acesso, ou um código enviado para o celular (via SMS ou aplicativo autenticador).

1. **Algo que você é**:
    - Usa características biométricas únicas, como impressões digitais, reconhecimento facial, voz ou retina.

1. **Autenticação Multifator (MFA)**:
    - Combina dois ou mais dos métodos acima para aumentar a segurança.

### Tipos de Autenticação Comuns:

- **Login e Senha**:
    - Forma mais básica, mas menos segura se não for bem gerenciada.
- **Autenticação de Dois Fatores (2FA)**:
    - Combina senha com algo como um código de verificação enviado ao telefone.
- **Autenticação Biométrica**:
    - Utiliza características físicas, como impressão digital ou rosto.
- **Single Sign-On (SSO)**:
    - Permite acessar múltiplos sistemas com um único conjunto de credenciais.
- **Chaves de Segurança (U2F)**:
    - Dispositivos físicos como pendrives que precisam ser conectados para autenticar.

### Por que a autenticação é importante?

Ela protege sistemas contra acessos não autorizados, minimizando o risco de roubo de dados, fraudes e outros tipos de ataques cibernéticos. A segurança da autenticação está diretamente ligada à escolha de métodos apropriados para cada contexto e à implementação de boas práticas, como a utilização de senhas fortes e ferramentas atualizadas.

### Tipos de Autenticação Explicados:

#### 1. **Login e Senha**

- **Como funciona**: O usuário insere um nome de usuário e uma senha previamente cadastrados.
- **Vantagens**:
    - Simples de implementar e usar.
    - Amplamente conhecido e adotado.
- **Desvantagens**:
    - Vulnerável a ataques de força bruta, phishing, ou vazamento de senhas.
    - Se uma senha for fraca ou reutilizada, compromete a segurança.

---

#### 2. **Autenticação de Dois Fatores (2FA)**

- **Como funciona**: Combina dois métodos de autenticação, geralmente:
    1. **Algo que você sabe** (senha).
    2. **Algo que você possui** (código enviado por SMS, app autenticador, ou chave física).
- **Exemplo**: Você faz login com sua senha e, em seguida, digita um código recebido no celular.
- **Vantagens**:
    - Aumenta a segurança, mesmo que a senha seja comprometida.
    - Comum em bancos e e-mails.
- **Desvantagens**:
    - Pode ser inconveniente se o usuário perder o dispositivo.
    - Mensagens SMS são vulneráveis a interceptação (SIM Swap).

---

#### 3. **Autenticação Biométrica**

- **Como funciona**: Utiliza características físicas únicas, como:
    - Impressão digital.
    - Reconhecimento facial.
    - Escaneamento de íris ou retina.
    - Reconhecimento de voz.
- **Exemplo**: Desbloqueio de celulares usando impressão digital ou rosto.
- **Vantagens**:
    - Difícil de falsificar.
    - Conveniente, pois elimina a necessidade de lembrar senhas.
- **Desvantagens**:
    - Pode falhar em certas condições (dedos molhados, luz inadequada, etc.).
    - Dados biométricos, se vazados, não podem ser "trocados" como senhas.

---

#### 4. **Single Sign-On (SSO)**

- **Como funciona**: Permite que um usuário acesse vários sistemas ou aplicativos com um único conjunto de credenciais.
- **Exemplo**: Usar sua conta do Google para entrar em vários serviços como YouTube, Gmail, ou aplicativos de terceiros.
- **Vantagens**:
    - Conveniência, pois reduz o número de senhas que o usuário precisa gerenciar.
    - Menos problemas com "esqueci minha senha".
- **Desvantagens**:
    - Se a conta principal for comprometida, todos os serviços associados ficam vulneráveis.

---

#### 5. **Chaves de Segurança (U2F)**

- **Como funciona**: Usa um dispositivo físico (como um pendrive) que precisa ser conectado ou aproximado do dispositivo de login.
- **Exemplo**: Uma chave USB YubiKey ou um dispositivo com NFC.
- **Vantagens**:
    - Proteção robusta contra phishing e ataques remotos.
    - Ideal para acessos corporativos ou críticos.
- **Desvantagens**:
    - Requer que o usuário tenha sempre o dispositivo em mãos.
    - Pode ser caro para implementação em larga escala.

---

#### 6. **Autenticação por Código Temporário (TOTP ou HOTP)**

- **Como funciona**: Gera códigos de acesso únicos que expiram rapidamente (geralmente 30 segundos). Esses códigos são fornecidos por aplicativos como Google Authenticator ou Authy.
- **Vantagens**:
    - Mais seguro que SMS, pois não depende da rede celular.
- **Desvantagens**:
    - Perda do aplicativo ou do dispositivo pode causar problemas de acesso.

---

#### 7. **Autenticação por Token (JWT, OAuth)**

- **Como funciona**: Após o login, o usuário recebe um "token" digital que serve como prova de autenticação. Este token pode ser usado para acessar diferentes partes do sistema sem repetir o login.
- **Exemplo**: Usado em APIs e integrações com terceiros.
- **Vantagens**:
    - Evita armazenar credenciais em todas as requisições.
- **Desvantagens**:
    - Exige cuidado com o armazenamento seguro do token.

---

#### 8. **Reconhecimento de Dispositivos**

- **Como funciona**: Usa características específicas de um dispositivo (como endereço MAC, localização, ou histórico) para autenticar o usuário.
- **Exemplo**: Um banco reconhecendo seu celular como "dispositivo confiável".
- **Vantagens**:
    - Conveniente para o usuário.
- **Desvantagens**:
    - Mudanças de dispositivo podem exigir reconfiguração.
    - Vulnerável se o dispositivo for roubado.

---

#### 9. **Autenticação Baseada em Contexto**

- **Como funciona**: Analisa o contexto do acesso, como:
    - Localização geográfica.
    - Dispositivo usado.
    - Horário do acesso.
- **Exemplo**: Bloquear login vindo de um país diferente do habitual.
- **Vantagens**:
    - Protege contra atividades suspeitas.
- **Desvantagens**:
    - Pode causar falsos positivos, bloqueando usuários legítimos.