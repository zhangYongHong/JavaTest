>>获取本地主机域名和ip



    import java.net.*;

    public class InetAddressDemo {

	/**
	 * @param args
	 */
	public static void main(String[] args) {
		// TODO Auto-generated method stub
         try {
			InetAddress inet1 = InetAddress.getByName("www.baidu.com");
			System.out.println(inet1);
			InetAddress inet2 = InetAddress.getByName("127.0.0.1");
			System.out.println(inet2);
			InetAddress inet3 = InetAddress.getLocalHost();
			System.out.println(inet3);
			
			String host = inet3.getHostName();
			System.out.println("域名: " + host);
			
			String ip = inet3.getHostAddress();
			System.out.println("IP:" + ip);
			 	 
		} catch (Exception e) {
			// TODO: handle exception
		}
		
	}

}

