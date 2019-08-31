	package InetAddress;

	import java.io.*;
	import java.net.*;

	public class SimpleSocketServer {
	
		/**
		 * @param args
		 */
		public static void main(String[] args) {
			// TODO Auto-generated method stub
			ServerSocket  serverSocket = null;
			Socket socket = null;
			OutputStream os = null;
			InputStream is = null;
			
			int port = 10000;
			try {
				serverSocket  = new ServerSocket(port);
				socket = serverSocket.accept();
				is = socket.getInputStream();
				byte[] b = new byte[1024];
				int n = is.read(b);
				System.out.println("客户端发送的内容为："  + new String(b, 0, n));
				os = socket.getOutputStream();
				os.write(b, 0, n);
			} catch (Exception e) {
				// TODO: handle exception
				e.printStackTrace();
			}finally{
					try {
					os.close();
					is.close();
					socket.close();
					serverSocket.close();
					
				} catch (Exception e2) {
					// TODO: handle exception
					e2.printStackTrace();
				}
			}
		}
	}
